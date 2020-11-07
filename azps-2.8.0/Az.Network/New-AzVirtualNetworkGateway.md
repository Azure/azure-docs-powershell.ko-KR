---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 75857d2c97ace9b06e3f7cdd7f672ac35a6fe34e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869830"
---
# <span data-ttu-id="f8464-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8464-102">SYNOPSIS</span></span>
<span data-ttu-id="f8464-103">가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="f8464-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="f8464-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8464-104">SYNTAX</span></span>

### <span data-ttu-id="f8464-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8464-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8464-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8464-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8464-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8464-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8464-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f8464-108">DESCRIPTION</span></span>
<span data-ttu-id="f8464-109">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f8464-110">**AzVirtualNetworkGateway** Cmdlet은 이름, 리소스 그룹 이름, 위치 및 IP 구성, 게이트웨이 유형 및 vpn 종류를 기반으로 하 여 Azure에서 게이트웨이의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="f8464-111">게이트웨이 SKU의 이름을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="f8464-112">이 게이트웨이를 사이트 간 연결에 사용 하는 경우 연결 클라이언트에 주소를 할당할 VPN 클라이언트 주소 풀과 게이트웨이에 연결 하는 VPN 클라이언트를 인증 하는 데 사용 되는 VPN 클라이언트 루트 인증서도 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="f8464-113">또한 BGP 및 Active-활성 등의 다른 기능을 포함 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="f8464-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f8464-114">EXAMPLES</span></span>

### <span data-ttu-id="f8464-115">1: 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="f8464-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f8464-116">위의 방법을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, Azure에서 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8464-117">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig" 변수에 저장 된 이전에 만든 IP 구성과 "VPN" 게이트웨이 형식, vpn 유형 "RouteBased" 및 sku "기본"으로 되어 있는 "이름"으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="f8464-118">2: 외부 Radius 구성을 사용 하 여 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="f8464-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f8464-119">위의 방법을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, Azure에서 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8464-120">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig" 변수에 저장 된 이전에 만든 IP 구성과 "VPN" 게이트웨이 형식, vpn 유형 "RouteBased" 및 sku "기본"으로 되어 있는 "이름"으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f8464-121">또한 주소가 "TestRadiusServer" 인 외부 radius 서버를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="f8464-122">또한 게이트웨이에서 고객에 의해 지정 된 사용자 지정 경로도 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f8464-123">3: P2S 설정을 사용 하 여 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="f8464-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
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

<span data-ttu-id="f8464-124">위의 작업을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, P2S 설정 (예: VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy 등)이 포함 된 가상 네트워크 게이트웨이를 Azure에서 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="f8464-125">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig" 변수에 저장 된 이전에 만든 IP 구성과 "VPN" 게이트웨이 형식, vpn 유형 "RouteBased" 및 sku "VpnGw1" 중에서 "\"로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="f8464-126">VpnProtocol (Ikev2로 설정), VpnClientAddressPool "201.169.0.0/16", VpnClientRootCertificate set 전달 됨: clientRootCertName 및 사용자 지정 vpn ipsec 정책에 따라 개체에 전달 되는 vpn 설정이 게이트웨이에서 설정 됩니다. $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="f8464-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="f8464-127">또한 게이트웨이에서 고객에 의해 지정 된 사용자 지정 경로도 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f8464-128">4: 가상 네트워크 게이트웨이의 VpnClient에 대 한 AAD 인증 구성을 사용 하 여 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="f8464-129">위의 방법을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, Azure에서 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8464-130">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig" 변수에 저장 된 이전에 만든 IP 구성과 "VPN" 게이트웨이 형식, vpn 유형 "RouteBased" 및 sku "기본"으로 되어 있는 "이름"으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f8464-131">또한 가상 네트워크 게이트웨이의 VpnClient에 대 한 AAD 인증 구성 AadTenantUri, AadIssuerUri 및 AadAudienceId를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="f8464-132">5: VpnGatewayGeneration를 사용 하 여 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="f8464-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f8464-133">위의 방법을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, Azure에서 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8464-134">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig", "VPN"의 게이트웨이 유형, vpn 유형 "RouteBased", sku "VpnGw4" 및 VpnGatewayGeneration Generation2 enabled로 저장 된 이전에 만든 IP 구성을 사용 하는 위치에 있는 "이름"으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="f8464-135">변수</span><span class="sxs-lookup"><span data-stu-id="f8464-135">PARAMETERS</span></span>

### <span data-ttu-id="f8464-136">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="f8464-136">-AadAudienceId</span></span>
<span data-ttu-id="f8464-137">P2S AAD 인증 옵션: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="f8464-137">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="f8464-138">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="f8464-138">-AadIssuerUri</span></span>
<span data-ttu-id="f8464-139">P2S AAD 인증 옵션: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="f8464-139">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="f8464-140">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="f8464-140">-AadTenantUri</span></span>
<span data-ttu-id="f8464-141">P2S AAD 인증 옵션: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="f8464-141">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="f8464-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8464-142">-AsJob</span></span>
<span data-ttu-id="f8464-143">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f8464-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8464-144">-Asn</span><span class="sxs-lookup"><span data-stu-id="f8464-144">-Asn</span></span>

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

### <span data-ttu-id="f8464-145">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="f8464-145">-CustomRoute</span></span>
<span data-ttu-id="f8464-146">고객이 지정한 사용자 지정 경로 AddressPool</span><span class="sxs-lookup"><span data-stu-id="f8464-146">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="f8464-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8464-147">-DefaultProfile</span></span>
<span data-ttu-id="f8464-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8464-149">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="f8464-149">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="f8464-150">활성 활성 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-150">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="f8464-151">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f8464-151">-EnableBgp</span></span>

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

### <span data-ttu-id="f8464-152">-Force</span><span class="sxs-lookup"><span data-stu-id="f8464-152">-Force</span></span>
<span data-ttu-id="f8464-153">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-153">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8464-154">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="f8464-154">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="f8464-155">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="f8464-155">-GatewaySku</span></span>

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

### <span data-ttu-id="f8464-156">-게이트웨이 종류</span><span class="sxs-lookup"><span data-stu-id="f8464-156">-GatewayType</span></span>

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

### <span data-ttu-id="f8464-157">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="f8464-157">-IpConfigurations</span></span>

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

### <span data-ttu-id="f8464-158">-위치</span><span class="sxs-lookup"><span data-stu-id="f8464-158">-Location</span></span>

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

### <span data-ttu-id="f8464-159">-이름</span><span class="sxs-lookup"><span data-stu-id="f8464-159">-Name</span></span>

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

### <span data-ttu-id="f8464-160">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f8464-160">-PeerWeight</span></span>

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

### <span data-ttu-id="f8464-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f8464-161">-RadiusServerAddress</span></span>
<span data-ttu-id="f8464-162">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="f8464-163">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f8464-163">-RadiusServerSecret</span></span>
<span data-ttu-id="f8464-164">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="f8464-164">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="f8464-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8464-165">-ResourceGroupName</span></span>

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

### <span data-ttu-id="f8464-166">태그</span><span class="sxs-lookup"><span data-stu-id="f8464-166">-Tag</span></span>
<span data-ttu-id="f8464-167">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-167">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f8464-168">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f8464-168">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f8464-169">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f8464-169">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="f8464-170">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f8464-170">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f8464-171">P2S VPN 클라이언트 터널링 프로토콜에 대 한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-171">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f8464-172">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="f8464-172">-VpnClientProtocol</span></span>
<span data-ttu-id="f8464-173">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="f8464-173">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="f8464-174">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="f8464-174">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="f8464-175">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="f8464-175">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="f8464-176">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f8464-176">-VpnGatewayGeneration</span></span>
<span data-ttu-id="f8464-177">이 VirtualNetwork VPN 게이트웨이의 세대입니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-177">The generation for this VirtualNetwork VPN gateway.</span></span> <span data-ttu-id="f8464-178">(%)은 (는)이 (가) VPN이 아닌 경우 없음 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-178">Must be None if GatewayType is not VPN.</span></span> <span data-ttu-id="f8464-179">설정한 후에는 게이트웨이 수명 동안이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-179">Once set, this property cannot be changed over the lifetime of the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, Generation1, Generation2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8464-180">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f8464-180">-VpnType</span></span>

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

### <span data-ttu-id="f8464-181">-확인</span><span class="sxs-lookup"><span data-stu-id="f8464-181">-Confirm</span></span>
<span data-ttu-id="f8464-182">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8464-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8464-183">-WhatIf</span></span>
<span data-ttu-id="f8464-184">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8464-185">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8464-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8464-186">CommonParameters</span></span>
<span data-ttu-id="f8464-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8464-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8464-188">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8464-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8464-189">입력</span><span class="sxs-lookup"><span data-stu-id="f8464-189">INPUTS</span></span>

### <span data-ttu-id="f8464-190">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f8464-190">System.String</span></span>

### <span data-ttu-id="f8464-191">PSVirtualNetworkGatewayIpConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f8464-191">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="f8464-192">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f8464-192">System.Boolean</span></span>

### <span data-ttu-id="f8464-193">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-193">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f8464-194">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="f8464-194">System.String[]</span></span>

### <span data-ttu-id="f8464-195">PSVpnClientRootCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f8464-195">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="f8464-196">PSVpnClientRevokedCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f8464-196">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="f8464-197">PSIpsecPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f8464-197">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f8464-198">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="f8464-198">System.UInt32</span></span>

### <span data-ttu-id="f8464-199">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="f8464-199">System.Int32</span></span>

### <span data-ttu-id="f8464-200">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="f8464-200">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f8464-201">System.webserver</span><span class="sxs-lookup"><span data-stu-id="f8464-201">System.Security.SecureString</span></span>

## <span data-ttu-id="f8464-202">출력</span><span class="sxs-lookup"><span data-stu-id="f8464-202">OUTPUTS</span></span>

### <span data-ttu-id="f8464-203">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f8464-203">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8464-204">상속자</span><span class="sxs-lookup"><span data-stu-id="f8464-204">NOTES</span></span>

## <span data-ttu-id="f8464-205">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8464-205">RELATED LINKS</span></span>

[<span data-ttu-id="f8464-206">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-206">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f8464-207">제거-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-207">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f8464-208">다시 설정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-208">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f8464-209">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-209">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f8464-210">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8464-210">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
