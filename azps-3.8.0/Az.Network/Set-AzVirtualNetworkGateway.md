---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: e5216d3a5727c32bd5e9f185cd48ace068a890b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034125"
---
# <span data-ttu-id="87dd7-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87dd7-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="87dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="87dd7-103">가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="87dd7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87dd7-104">SYNTAX</span></span>

### <span data-ttu-id="87dd7-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="87dd7-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87dd7-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="87dd7-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87dd7-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="87dd7-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87dd7-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="87dd7-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87dd7-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="87dd7-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87dd7-110">설명은</span><span class="sxs-lookup"><span data-stu-id="87dd7-110">DESCRIPTION</span></span>
<span data-ttu-id="87dd7-111">**AzVirtualNetworkGateway** cmdlet은 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="87dd7-112">예제의</span><span class="sxs-lookup"><span data-stu-id="87dd7-112">EXAMPLES</span></span>

### <span data-ttu-id="87dd7-113">예제 1: 가상 네트워크 게이트웨이의 ASN 업데이트</span><span class="sxs-lookup"><span data-stu-id="87dd7-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="87dd7-114">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져와 $Gateway 이라는 변수에 저장 하 고 두 번째 명령이 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="87dd7-115">또한이 명령은 ASN을 1337로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="87dd7-116">예제 2: 가상 네트워크 게이트웨이에 IPsec 정책 추가</span><span class="sxs-lookup"><span data-stu-id="87dd7-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="87dd7-117">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령은 지정 된 ipsec 매개 변수로 Vpn ipsec 정책 개체를 만드는 $Gateway 명명 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="87dd7-118">세 번째 명령은 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="87dd7-119">또한이 명령은 가상 네트워크 게이트웨이의 $vpnclientipsecpolicy 개체에 지정 된 사용자 지정 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="87dd7-120">예제 3: 기존 가상 네트워크 게이트웨이에 태그 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="87dd7-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="87dd7-121">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령이 @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} 태그를 사용 하 여 가상 네트워크 게이트웨이 Gateway01를 업데이트 하는 변수를 $Gateway 이름에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="87dd7-122">예제 4: 기존 가상 네트워크 게이트웨이의 VpnClient에 대 한 AAD 인증 구성 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="87dd7-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="87dd7-123">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령이 AAD 인증 구성 params: aadTenantUri, aadAudienceId, aadIssuerUri에 대 한 가상 네트워크 게이트웨이 Gateway01를 업데이트 하 여이를 $Gateway 명명 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="87dd7-124">세 번째 명령은 가상 네트워크 게이트웨이의 VpnClient에서 AAD 인증 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="87dd7-125">예제 5: 기존 가상 네트워크 게이트웨이에 IpConfigurationBgpPeeringAddresses 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="87dd7-125">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="87dd7-126">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령이 가상 네트워크 게이트웨이 Gateway01 IpConfiguration Id의 값을 변수 ipconfigurationId1에 할당 하 여 $Gateway 명명 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-126">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="87dd7-127">세 번째 명령은 addresslist1에 주소 목록을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-127">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="87dd7-128">네 번째 명령은 PSIpConfigurationBgpPeeringAddress 개체를 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-128">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="87dd7-129">다섯 번째 명령은 새로 만든 PSIpConfigurationBgpPeeringAddress을 IpConfigurationBgpPeeringAddresses 하 고 게이트웨이를 업데이트 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-129">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="87dd7-130">변수</span><span class="sxs-lookup"><span data-stu-id="87dd7-130">PARAMETERS</span></span>

### <span data-ttu-id="87dd7-131">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="87dd7-131">-AadAudienceId</span></span>
<span data-ttu-id="87dd7-132">P2S AAD 인증 옵션: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="87dd7-132">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="87dd7-133">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="87dd7-133">-AadIssuerUri</span></span>
<span data-ttu-id="87dd7-134">P2S AAD 인증 옵션: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="87dd7-134">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="87dd7-135">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="87dd7-135">-AadTenantUri</span></span>
<span data-ttu-id="87dd7-136">P2S AAD 인증 옵션: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="87dd7-136">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="87dd7-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87dd7-137">-AsJob</span></span>
<span data-ttu-id="87dd7-138">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="87dd7-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87dd7-139">-Asn</span><span class="sxs-lookup"><span data-stu-id="87dd7-139">-Asn</span></span>
<span data-ttu-id="87dd7-140">가상 네트워크 게이트웨이의 ASN (IPsec 터널 내에서 BGP 세션을 설정 하는 데 사용 됨)</span><span class="sxs-lookup"><span data-stu-id="87dd7-140">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="87dd7-141">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="87dd7-141">-CustomRoute</span></span>
<span data-ttu-id="87dd7-142">고객이 지정한 사용자 지정 경로 AddressPool</span><span class="sxs-lookup"><span data-stu-id="87dd7-142">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="87dd7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87dd7-143">-DefaultProfile</span></span>
<span data-ttu-id="87dd7-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87dd7-145">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="87dd7-145">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="87dd7-146">가상 네트워크 게이트웨이에서 활성 활성 기능을 사용 하지 않도록 설정 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="87dd7-146">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="87dd7-147">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="87dd7-147">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="87dd7-148">가상 네트워크 게이트웨이에서 활성 활성 기능을 사용 하도록 설정 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="87dd7-148">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="87dd7-149">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="87dd7-149">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="87dd7-150">가상 네트워크 게이트웨이에서 활성 활성 기능을 사용 하도록 설정 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="87dd7-150">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87dd7-151">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="87dd7-151">-GatewayDefaultSite</span></span>
<span data-ttu-id="87dd7-152">강제 터널링에 사용할 기본 사이트입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-152">The default site to use for force tunneling.</span></span>
<span data-ttu-id="87dd7-153">기본 사이트를 지정 하면 게이트웨이 vnet의 모든 인터넷 트래픽이 해당 사이트로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-153">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="87dd7-154">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="87dd7-154">-GatewaySku</span></span>
<span data-ttu-id="87dd7-155">가상 네트워크 게이트웨이의 SKU</span><span class="sxs-lookup"><span data-stu-id="87dd7-155">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="87dd7-156">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="87dd7-156">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="87dd7-157">가상 네트워크 게이트웨이 bgpsettings에 대 한 BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="87dd7-157">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="87dd7-158">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="87dd7-158">-PeerWeight</span></span>
<span data-ttu-id="87dd7-159">이 가상 네트워크 게이트웨이에서 BGP를 통해 얻은 경로에 추가 된 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-159">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="87dd7-160">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="87dd7-160">-RadiusServerAddress</span></span>
<span data-ttu-id="87dd7-161">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-161">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87dd7-162">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="87dd7-162">-RadiusServerSecret</span></span>
<span data-ttu-id="87dd7-163">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="87dd7-163">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87dd7-164">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="87dd7-164">-RemoveAadAuthentication</span></span>
<span data-ttu-id="87dd7-165">가상 네트워크 게이트웨이에서 P2S 클라이언트에 대 한 AAD 인증을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-165">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="87dd7-166">태그</span><span class="sxs-lookup"><span data-stu-id="87dd7-166">-Tag</span></span>
<span data-ttu-id="87dd7-167">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-167">P2S External Radius server address.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87dd7-168">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87dd7-168">-VirtualNetworkGateway</span></span>
<span data-ttu-id="87dd7-169">수정이 해제 된 가상 네트워크 게이트웨이 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-169">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="87dd7-170">Get-AzVirtualNetworkGateway를 사용 하 여 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-170">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87dd7-171">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="87dd7-171">-VpnClientAddressPool</span></span>
<span data-ttu-id="87dd7-172">VPN 클라이언트 IP 주소를 할당할 주소 공간입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-172">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="87dd7-173">이는 가상 네트워크 또는 온-프레미스 범위와 중복 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-173">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="87dd7-174">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="87dd7-174">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="87dd7-175">P2S VPN 클라이언트 터널링 프로토콜에 대 한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-175">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="87dd7-176">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="87dd7-176">-VpnClientProtocol</span></span>
<span data-ttu-id="87dd7-177">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="87dd7-177">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="87dd7-178">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="87dd7-178">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="87dd7-179">해지 된 VPN 클라이언트 인증서의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-179">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="87dd7-180">이들 중 하 나와 일치 하는 인증서를 제시 하는 VPN 클라이언트는 자리 비움 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-180">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="87dd7-181">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="87dd7-181">-VpnClientRootCertificates</span></span>
<span data-ttu-id="87dd7-182">VPN 클라이언트 인증에 사용할 VPN 클라이언트 루트 인증서의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-182">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="87dd7-183">VPN 클라이언트를 연결 하는 것은 이러한 루트 인증서 중 하나에서 생성 된 인증서를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-183">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="87dd7-184">-확인</span><span class="sxs-lookup"><span data-stu-id="87dd7-184">-Confirm</span></span>
<span data-ttu-id="87dd7-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87dd7-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87dd7-186">-WhatIf</span></span>
<span data-ttu-id="87dd7-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87dd7-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87dd7-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87dd7-189">CommonParameters</span></span>
<span data-ttu-id="87dd7-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87dd7-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87dd7-191">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="87dd7-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87dd7-192">입력</span><span class="sxs-lookup"><span data-stu-id="87dd7-192">INPUTS</span></span>

### <span data-ttu-id="87dd7-193">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="87dd7-193">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="87dd7-194">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87dd7-194">System.String</span></span>

### <span data-ttu-id="87dd7-195">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87dd7-195">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="87dd7-196">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="87dd7-196">System.String[]</span></span>

### <span data-ttu-id="87dd7-197">PSVpnClientRootCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="87dd7-197">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="87dd7-198">PSVpnClientRevokedCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="87dd7-198">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="87dd7-199">PSIpsecPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="87dd7-199">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="87dd7-200">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="87dd7-200">System.UInt32</span></span>

### <span data-ttu-id="87dd7-201">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="87dd7-201">System.Int32</span></span>

### <span data-ttu-id="87dd7-202">PSIpConfigurationBgpPeeringAddress [] (으)로</span><span class="sxs-lookup"><span data-stu-id="87dd7-202">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="87dd7-203">System.webserver</span><span class="sxs-lookup"><span data-stu-id="87dd7-203">System.Security.SecureString</span></span>

## <span data-ttu-id="87dd7-204">출력</span><span class="sxs-lookup"><span data-stu-id="87dd7-204">OUTPUTS</span></span>

### <span data-ttu-id="87dd7-205">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="87dd7-205">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="87dd7-206">상속자</span><span class="sxs-lookup"><span data-stu-id="87dd7-206">NOTES</span></span>

## <span data-ttu-id="87dd7-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87dd7-207">RELATED LINKS</span></span>
