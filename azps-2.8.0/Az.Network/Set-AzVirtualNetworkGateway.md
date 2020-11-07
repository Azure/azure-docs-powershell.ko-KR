---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872145"
---
# <span data-ttu-id="8f900-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="8f900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f900-102">SYNOPSIS</span></span>
<span data-ttu-id="8f900-103">가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="8f900-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f900-104">SYNTAX</span></span>

### <span data-ttu-id="8f900-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f900-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f900-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f900-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f900-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="8f900-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f900-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f900-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f900-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="8f900-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f900-110">설명은</span><span class="sxs-lookup"><span data-stu-id="8f900-110">DESCRIPTION</span></span>
<span data-ttu-id="8f900-111">**AzVirtualNetworkGateway** cmdlet은 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="8f900-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8f900-112">EXAMPLES</span></span>

### <span data-ttu-id="8f900-113">예제 1: 가상 네트워크 게이트웨이의 ASN 업데이트</span><span class="sxs-lookup"><span data-stu-id="8f900-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="8f900-114">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져와 $Gateway 이라는 변수에 저장 하 고 두 번째 명령이 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="8f900-115">또한이 명령은 ASN을 1337로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="8f900-116">예제 2: 가상 네트워크 게이트웨이에 IPsec 정책 추가</span><span class="sxs-lookup"><span data-stu-id="8f900-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="8f900-117">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령은 지정 된 ipsec 매개 변수로 Vpn ipsec 정책 개체를 만드는 $Gateway 명명 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="8f900-118">세 번째 명령은 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="8f900-119">또한이 명령은 가상 네트워크 게이트웨이의 $vpnclientipsecpolicy 개체에 지정 된 사용자 지정 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="8f900-120">예제 3: 기존 가상 네트워크 게이트웨이에 태그 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="8f900-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="8f900-121">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령이 @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"} 태그를 사용 하 여 가상 네트워크 게이트웨이 Gateway01를 업데이트 하는 변수를 $Gateway 이름에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="8f900-122">예제 4: 기존 가상 네트워크 게이트웨이의 VpnClient에 대 한 AAD 인증 구성 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="8f900-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="8f900-123">첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령이 AAD 인증 구성 params: aadTenantUri, aadAudienceId, aadIssuerUri에 대 한 가상 네트워크 게이트웨이 Gateway01를 업데이트 하 여이를 $Gateway 명명 된 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="8f900-124">세 번째 명령은 가상 네트워크 게이트웨이의 VpnClient에서 AAD 인증 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="8f900-125">변수</span><span class="sxs-lookup"><span data-stu-id="8f900-125">PARAMETERS</span></span>

### <span data-ttu-id="8f900-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="8f900-126">-AadAudienceId</span></span>
<span data-ttu-id="8f900-127">P2S AAD 인증 옵션: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="8f900-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="8f900-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="8f900-128">-AadIssuerUri</span></span>
<span data-ttu-id="8f900-129">P2S AAD 인증 옵션: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="8f900-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="8f900-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="8f900-130">-AadTenantUri</span></span>
<span data-ttu-id="8f900-131">P2S AAD 인증 옵션: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="8f900-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="8f900-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f900-132">-AsJob</span></span>
<span data-ttu-id="8f900-133">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8f900-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f900-134">-Asn</span><span class="sxs-lookup"><span data-stu-id="8f900-134">-Asn</span></span>
<span data-ttu-id="8f900-135">IPsec 터널 내에서 BGP (Border Gateway Protocol) 세션을 설정 하는 데 사용 되는 가상 ASN (네트워크 게이트웨이 익명 시스템 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="8f900-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="8f900-136">-CustomRoute</span></span>
<span data-ttu-id="8f900-137">고객이 지정한 사용자 지정 경로 AddressPool</span><span class="sxs-lookup"><span data-stu-id="8f900-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="8f900-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f900-138">-DefaultProfile</span></span>
<span data-ttu-id="8f900-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f900-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="8f900-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="8f900-141">활성 활성 기능을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="8f900-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="8f900-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="8f900-143">활성 활성 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="8f900-144">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="8f900-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="8f900-145">강제 터널링에 사용할 기본 사이트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="8f900-146">기본 사이트를 지정 하면 게이트웨이의 VPN (가상 사설망)에 있는 모든 인터넷 트래픽이 해당 사이트로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="8f900-147">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="8f900-147">-GatewaySku</span></span>
<span data-ttu-id="8f900-148">가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="8f900-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f900-150">기본적</span><span class="sxs-lookup"><span data-stu-id="8f900-150">Basic</span></span>
- <span data-ttu-id="8f900-151">표준이</span><span class="sxs-lookup"><span data-stu-id="8f900-151">Standard</span></span>
- <span data-ttu-id="8f900-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="8f900-152">HighPerformance</span></span>
- <span data-ttu-id="8f900-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="8f900-153">VpnGw1</span></span>
- <span data-ttu-id="8f900-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="8f900-154">VpnGw2</span></span>
- <span data-ttu-id="8f900-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="8f900-155">VpnGw3</span></span>
- <span data-ttu-id="8f900-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="8f900-156">VpnGw1AZ</span></span>
- <span data-ttu-id="8f900-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="8f900-157">VpnGw2AZ</span></span>
- <span data-ttu-id="8f900-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="8f900-158">VpnGw3AZ</span></span>
- <span data-ttu-id="8f900-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="8f900-159">ErGw1AZ</span></span>
- <span data-ttu-id="8f900-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="8f900-160">ErGw2AZ</span></span>
- <span data-ttu-id="8f900-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="8f900-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="8f900-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="8f900-162">-PeerWeight</span></span>
<span data-ttu-id="8f900-163">이 가상 네트워크 게이트웨이에서 BGP를 통해 얻은 경로에 추가 된 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="8f900-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="8f900-164">-RadiusServerAddress</span></span>
<span data-ttu-id="8f900-165">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-165">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="8f900-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="8f900-166">-RadiusServerSecret</span></span>
<span data-ttu-id="8f900-167">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="8f900-167">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="8f900-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="8f900-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="8f900-169">가상 네트워크 게이트웨이에서 P2S 클라이언트에 대 한 AAD 인증을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="8f900-170">태그</span><span class="sxs-lookup"><span data-stu-id="8f900-170">-Tag</span></span>
<span data-ttu-id="8f900-171">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-171">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8f900-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="8f900-173">수정이 해제 되는 가상 네트워크 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="8f900-174">Get-AzVirtualNetworkGateway cmdlet을 사용 하 여 가상 네트워크 게이트웨이 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="8f900-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="8f900-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="8f900-176">이 cmdlet이 VPN 클라이언트 IP 주소를 할당 하는 데 사용 하는 주소 공간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="8f900-177">이는 가상 네트워크 또는 온-프레미스 범위와 중복 되어서는 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="8f900-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="8f900-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="8f900-179">P2S VPN 클라이언트 터널링 프로토콜에 대 한 IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="8f900-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="8f900-180">-VpnClientProtocol</span></span>
<span data-ttu-id="8f900-181">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="8f900-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="8f900-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="8f900-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="8f900-183">해지 된 VPN 클라이언트 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="8f900-184">이들 중 하 나와 일치 하는 인증서를 제시 하는 VPN 클라이언트는 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="8f900-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="8f900-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="8f900-186">VPN 클라이언트 인증에 사용할 VPN 클라이언트 루트 인증서의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="8f900-187">VPN 클라이언트를 연결 하는 것은 이러한 루트 인증서 중 하나에서 생성 된 인증서를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="8f900-188">-확인</span><span class="sxs-lookup"><span data-stu-id="8f900-188">-Confirm</span></span>
<span data-ttu-id="8f900-189">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f900-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f900-190">-WhatIf</span></span>
<span data-ttu-id="8f900-191">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f900-192">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f900-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f900-193">CommonParameters</span></span>
<span data-ttu-id="8f900-194">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f900-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f900-195">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f900-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f900-196">입력</span><span class="sxs-lookup"><span data-stu-id="8f900-196">INPUTS</span></span>

### <span data-ttu-id="8f900-197">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8f900-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8f900-198">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f900-198">System.String</span></span>

### <span data-ttu-id="8f900-199">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="8f900-200">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="8f900-200">System.String[]</span></span>

### <span data-ttu-id="8f900-201">PSVpnClientRootCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="8f900-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="8f900-202">PSVpnClientRevokedCertificate [] (으)로</span><span class="sxs-lookup"><span data-stu-id="8f900-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="8f900-203">PSIpsecPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="8f900-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="8f900-204">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="8f900-204">System.UInt32</span></span>

### <span data-ttu-id="8f900-205">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="8f900-205">System.Int32</span></span>

### <span data-ttu-id="8f900-206">System.webserver</span><span class="sxs-lookup"><span data-stu-id="8f900-206">System.Security.SecureString</span></span>

## <span data-ttu-id="8f900-207">출력</span><span class="sxs-lookup"><span data-stu-id="8f900-207">OUTPUTS</span></span>

### <span data-ttu-id="8f900-208">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8f900-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8f900-209">상속자</span><span class="sxs-lookup"><span data-stu-id="8f900-209">NOTES</span></span>
* <span data-ttu-id="8f900-210">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="8f900-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8f900-211">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f900-211">RELATED LINKS</span></span>

[<span data-ttu-id="8f900-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8f900-213">새로운 AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8f900-214">제거-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8f900-215">다시 설정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8f900-216">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f900-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
