---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202731"
---
# <span data-ttu-id="a089b-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a089b-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a089b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a089b-102">SYNOPSIS</span></span>
<span data-ttu-id="a089b-103">Virtual Network 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="a089b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a089b-104">SYNTAX</span></span>

### <span data-ttu-id="a089b-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="a089b-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a089b-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="a089b-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a089b-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a089b-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a089b-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a089b-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a089b-109">설명</span><span class="sxs-lookup"><span data-stu-id="a089b-109">DESCRIPTION</span></span>
<span data-ttu-id="a089b-110">Virtual Network 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="a089b-111">**New-AzVirtualNetworkGateway** cmdlet은 이름, 리소스 그룹 이름, 위치 및 IP 구성뿐만 아니라 게이트웨이 유형 및 VPN인 경우 VPN 유형에 따라 Azure에서 게이트웨이 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="a089b-112">게이트웨이 SKU의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="a089b-113">지점 및 사이트 연결에 이 게이트웨이를 사용하는 경우 연결 클라이언트에 주소를 할당할 VPN 클라이언트 주소 풀과 게이트웨이에 연결되는 VPN 클라이언트를 인증하는 데 사용되는 VPN 클라이언트 루트 인증서를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="a089b-114">BGP 및 Active-Active와 같은 다른 기능을 포함 하게 선택할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="a089b-115">예제</span><span class="sxs-lookup"><span data-stu-id="a089b-115">EXAMPLES</span></span>

### <span data-ttu-id="a089b-116">예제 1: Virtual Network 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="a089b-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="a089b-117">위의 항목은 리소스 그룹을 만들고, 공용 IP 주소를 요청하고, Virtual Network 및 서브넷을 만들고, Azure에서 Virtual Network 게이트웨이를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="a089b-118">게이트웨이는 이전에 만든 IP 구성이 "ngwIPConfig" 변수에 저장된 "ngwIPConfig", 게이트웨이 유형 "RouteBased" 및 SKU "Basic"에 저장된 리소스 그룹 "vnet-gateway" 내에서 "myNGW"라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="a089b-119">예제 2: 외부 반경 구성을 사용하여 Virtual Network 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="a089b-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="a089b-120">위의 항목은 리소스 그룹을 만들고, 공용 IP 주소를 요청하고, Virtual Network 및 서브넷을 만들고, Azure에서 Virtual Network 게이트웨이를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="a089b-121">게이트웨이는 이전에 만든 IP 구성이 "ngwIPConfig" 변수에 저장된 "ngwIPConfig", 게이트웨이 유형 "RouteBased" 및 SKU "Basic"에 저장된 리소스 그룹 "vnet-gateway" 내에서 "myNGW"라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="a089b-122">또한 주소가 "TestRadiusServer"인 외부 반경 서버를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="a089b-123">또한 게이트웨이에서 고객이 지정한 사용자 지정 경로도 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="a089b-124">예제 3: P2S 설정을 사용하여 Virtual Network 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="a089b-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="a089b-125">위의 항목은 리소스 그룹을 만들고, 공용 IP 주소를 요청하고, Virtual Network 및 서브넷을 만들고, Azure에서 P2S 설정(예: VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy 등)을 사용하여 Virtual Network 게이트웨이를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="a089b-126">게이트웨이는 이전에 만든 IP 구성이 "ngwIPConfig" 변수에 저장된 "ngwIPConfig", 게이트웨이 유형 "RouteBased" 및 SKU "VpnGw1" 위치에 있는 리소스 그룹 "vnet-gateway" 내에서 "myNGW"라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="a089b-127">Vpn 설정은 게이트웨이에 Ikev2로 설정된 VpnProtocol, VpnClientAddressPool을 "201.169.0.0/16"으로 설정하고, 전달된 VpnClientRootCertificate 집합: clientRootCertName 및 object:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="a089b-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="a089b-128">또한 게이트웨이에서 고객이 지정한 사용자 지정 경로도 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="a089b-129">예제 4: 가상 네트워크 게이트웨이의 VpnClient에 대한 AAD 인증 구성을 사용하여 Virtual Network 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="a089b-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="a089b-130">위의 항목은 리소스 그룹을 만들고, 공용 IP 주소를 요청하고, Virtual Network 및 서브넷을 만들고, Azure에서 Virtual Network 게이트웨이를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="a089b-131">게이트웨이는 이전에 만든 IP 구성이 "ngwIPConfig" 변수에 저장된 "ngwIPConfig", 게이트웨이 유형 "RouteBased" 및 SKU "Basic"에 저장된 리소스 그룹 "vnet-gateway" 내에서 "myNGW"라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="a089b-132">또한 가상 네트워크 게이트웨이의 VpnClient에 대한 AadTenantUri, AadIssuerUri 및 AadAudienceId와 같은 AAD 인증 구성을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="a089b-133">예제 5: VpnGatewayGeneration을 사용하여 Virtual Network 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="a089b-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="a089b-134">위의 항목은 리소스 그룹을 만들고, 공용 IP 주소를 요청하고, Virtual Network 및 서브넷을 만들고, Azure에서 Virtual Network 게이트웨이를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="a089b-135">게이트웨이는 "ngwIPConfig" 변수에 저장된 이전에 만든 IP 구성, "VPN"의 게이트웨이 유형, "RouteBased", SKU "VpnGw4" 및 VpnGatewayGeneration Generation2가 활성화된 이전에 생성된 IP 구성을 사용하여 리소스 그룹 "vnet-gateway" 내에서 "myNGW"라고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="a089b-136">예제 6: IpConfigurationBgpPeeringAddresses를 사용하여 Virtual Network 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="a089b-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="a089b-137">위의 항목은 리소스 그룹을 만들고, 공용 IP 주소를 요청하고, Virtual Network 및 서브넷을 만들고, Azure에서 Virtual Network 게이트웨이를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="a089b-138">방금 만든 게이트웨이 ipconfiguration의 ipconfigurationId1은 ngwipconfig에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="a089b-139">게이트웨이는 이전에 만든 IP 구성 Bgppeering 주소가 "gw1ipconfBgp1" 변수에 저장된 위치 "UK West"의 리소스 그룹 "resourcegroup1resourcegroup1" 내에서 "gateway1"이라고 합니다. "VPN"의 게이트웨이 유형, VPN 유형 "RouteBased", SKU "VpnGw4" 및 VpnGatewayGeneration Generation2를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="a089b-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a089b-140">PARAMETERS</span></span>

### <span data-ttu-id="a089b-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="a089b-141">-AadAudienceId</span></span>
<span data-ttu-id="a089b-142">P2S AAD 인증 옵션:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="a089b-142">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="a089b-143">-AadIssuerUri</span></span>
<span data-ttu-id="a089b-144">P2S AAD 인증 옵션:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="a089b-144">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="a089b-145">-AadTenantUri</span></span>
<span data-ttu-id="a089b-146">P2S AAD 인증 옵션:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="a089b-146">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a089b-147">-AsJob</span></span>
<span data-ttu-id="a089b-148">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a089b-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a089b-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="a089b-149">-Asn</span></span>
<span data-ttu-id="a089b-150">VPN을 통해 BGP용 가상 네트워크 게이트웨이의 ASN</span><span class="sxs-lookup"><span data-stu-id="a089b-150">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="a089b-151">-CustomRoute</span></span>
<span data-ttu-id="a089b-152">고객이 지정한 사용자 지정 경로 AddressPool</span><span class="sxs-lookup"><span data-stu-id="a089b-152">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a089b-153">-DefaultProfile</span></span>
<span data-ttu-id="a089b-154">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a089b-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a089b-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="a089b-156">가상 네트워크 게이트웨이에서 활성 활성 기능을 사용하도록 설정하는 플래그</span><span class="sxs-lookup"><span data-stu-id="a089b-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="a089b-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a089b-157">-EnableBgp</span></span>
<span data-ttu-id="a089b-158">EnableBgp 플래그</span><span class="sxs-lookup"><span data-stu-id="a089b-158">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a089b-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="a089b-160">가상 네트워크 게이트웨이에서 개인 IPAddress를 사용하도록 설정하는 플래그</span><span class="sxs-lookup"><span data-stu-id="a089b-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="a089b-161">-Force</span><span class="sxs-lookup"><span data-stu-id="a089b-161">-Force</span></span>
<span data-ttu-id="a089b-162">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a089b-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a089b-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="a089b-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a089b-164">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a089b-165">-GatewaySku</span></span>
<span data-ttu-id="a089b-166">게이트웨이 SKU 계층</span><span class="sxs-lookup"><span data-stu-id="a089b-166">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="a089b-167">-GatewayType</span></span>
<span data-ttu-id="a089b-168">이 가상 네트워크 게이트웨이의 유형: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a089b-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="a089b-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="a089b-170">가상 네트워크 게이트웨이 bgpsettings에 대한 BgpPeeringAddresses입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="a089b-171">-IpConfigurations</span></span>
<span data-ttu-id="a089b-172">가상 네트워크 게이트웨이에 대한 IpConfigurations입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-172">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-173">-Location</span><span class="sxs-lookup"><span data-stu-id="a089b-173">-Location</span></span>
<span data-ttu-id="a089b-174">위치.</span><span class="sxs-lookup"><span data-stu-id="a089b-174">location.</span></span>

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

### <span data-ttu-id="a089b-175">-Name</span><span class="sxs-lookup"><span data-stu-id="a089b-175">-Name</span></span>
<span data-ttu-id="a089b-176">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-176">The resource name.</span></span>

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

### <span data-ttu-id="a089b-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a089b-177">-PeerWeight</span></span>
<span data-ttu-id="a089b-178">이 가상 네트워크 게이트웨이에서 BGP를 통해 학습된 경로에 추가된 가중치</span><span class="sxs-lookup"><span data-stu-id="a089b-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a089b-179">-RadiusServerAddress</span></span>
<span data-ttu-id="a089b-180">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-180">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="a089b-181">-RadiusServerList</span></span>
<span data-ttu-id="a089b-182">P2S 여러 외부 Radius 서버 서버.</span><span class="sxs-lookup"><span data-stu-id="a089b-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a089b-183">-RadiusServerSecret</span></span>
<span data-ttu-id="a089b-184">P2S 외부 Radius 서버 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-184">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a089b-185">-ResourceGroupName</span></span>
<span data-ttu-id="a089b-186">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-186">The resource group name.</span></span>

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

### <span data-ttu-id="a089b-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="a089b-187">-Tag</span></span>
<span data-ttu-id="a089b-188">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a089b-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a089b-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="a089b-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="a089b-190">P2S VpnClient AddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a089b-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a089b-192">P2S VPN 클라이언트 터널링 프로토콜에 대한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="a089b-193">-VpnClientProtocol</span></span>
<span data-ttu-id="a089b-194">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="a089b-194">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="a089b-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="a089b-196">해지할 VpnClientCertificates 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-196">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="a089b-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="a089b-198">추가할 VpnClientRootCertificates 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-198">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="a089b-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="a089b-200">이 VirtualNetwork VPN Gateway에 대한 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="a089b-201">GatewayType이 VPN이 아닌 경우 None이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="a089b-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="a089b-202">-VpnType</span></span>
<span data-ttu-id="a089b-203">Vpn:PolicyBased/RouteBased의 형식</span><span class="sxs-lookup"><span data-stu-id="a089b-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a089b-204">-Confirm</span></span>
<span data-ttu-id="a089b-205">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-205">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a089b-206">-WhatIf</span></span>
<span data-ttu-id="a089b-207">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a089b-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a089b-208">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-208">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a089b-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a089b-209">CommonParameters</span></span>
<span data-ttu-id="a089b-210">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a089b-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a089b-211">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a089b-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a089b-212">입력</span><span class="sxs-lookup"><span data-stu-id="a089b-212">INPUTS</span></span>

### <span data-ttu-id="a089b-213">System.String</span><span class="sxs-lookup"><span data-stu-id="a089b-213">System.String</span></span>

### <span data-ttu-id="a089b-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a089b-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="a089b-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a089b-215">System.Boolean</span></span>

### <span data-ttu-id="a089b-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a089b-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="a089b-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a089b-217">System.String[]</span></span>

### <span data-ttu-id="a089b-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="a089b-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="a089b-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="a089b-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="a089b-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="a089b-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="a089b-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="a089b-221">System.UInt32</span></span>

### <span data-ttu-id="a089b-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a089b-222">System.Int32</span></span>

### <span data-ttu-id="a089b-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="a089b-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="a089b-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a089b-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a089b-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="a089b-225">System.Security.SecureString</span></span>

## <span data-ttu-id="a089b-226">출력</span><span class="sxs-lookup"><span data-stu-id="a089b-226">OUTPUTS</span></span>

### <span data-ttu-id="a089b-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a089b-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a089b-228">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a089b-228">NOTES</span></span>

## <span data-ttu-id="a089b-229">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a089b-229">RELATED LINKS</span></span>
