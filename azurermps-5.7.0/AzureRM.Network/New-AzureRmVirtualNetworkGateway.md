---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 6f0a18211ae7c9d2fe8ffcb9c653de9952691e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533704"
---
# <span data-ttu-id="ad71d-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad71d-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="ad71d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad71d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad71d-103">가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="ad71d-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad71d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad71d-104">SYNTAX</span></span>

### <span data-ttu-id="ad71d-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad71d-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad71d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad71d-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad71d-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ad71d-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad71d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ad71d-108">DESCRIPTION</span></span>
<span data-ttu-id="ad71d-109">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="ad71d-110">**AzureRmVirtualNetworkGateway** Cmdlet은 이름, 리소스 그룹 이름, 위치 및 IP 구성, 게이트웨이 유형 및 vpn 종류를 기반으로 하 여 Azure에서 게이트웨이의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="ad71d-111">게이트웨이 SKU의 이름을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="ad71d-112">이 게이트웨이를 사이트 간 연결에 사용 하는 경우 연결 클라이언트에 주소를 할당할 VPN 클라이언트 주소 풀과 게이트웨이에 연결 하는 VPN 클라이언트를 인증 하는 데 사용 되는 VPN 클라이언트 루트 인증서도 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="ad71d-113">또한 BGP 및 Active-활성 등의 다른 기능을 포함 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="ad71d-114">예제의</span><span class="sxs-lookup"><span data-stu-id="ad71d-114">EXAMPLES</span></span>

### <span data-ttu-id="ad71d-115">1: 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="ad71d-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="ad71d-116">위의 방법을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, Azure에서 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="ad71d-117">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig" 변수에 저장 된 이전에 만든 IP 구성과 "VPN" 게이트웨이 형식, vpn 유형 "RouteBased" 및 sku "기본"으로 되어 있는 "이름"으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="ad71d-118">2: 외부 Radius 구성을 사용 하 여 가상 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="ad71d-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="ad71d-119">위의 방법을 통해 리소스 그룹을 만들고, 공용 IP 주소를 요청 하 고, 가상 네트워크와 서브넷을 만들고, Azure에서 가상 네트워크 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="ad71d-120">게이트웨이는 "영국 서쪽"의 리소스 그룹 "myNGW"에서 "ngwIPConfig" 변수에 저장 된 이전에 만든 IP 구성과 "VPN" 게이트웨이 형식, vpn 유형 "RouteBased" 및 sku "기본"으로 되어 있는 "이름"으로 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="ad71d-121">또한 주소가 "TestRadiusServer" 인 외부 radius 서버를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="ad71d-122">변수</span><span class="sxs-lookup"><span data-stu-id="ad71d-122">PARAMETERS</span></span>

### <span data-ttu-id="ad71d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad71d-123">-AsJob</span></span>
<span data-ttu-id="ad71d-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ad71d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad71d-125">-Asn</span><span class="sxs-lookup"><span data-stu-id="ad71d-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad71d-126">-DefaultProfile</span></span>
<span data-ttu-id="ad71d-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="ad71d-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="ad71d-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="ad71d-129">활성 활성 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="ad71d-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ad71d-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="ad71d-131">-Force</span></span>
<span data-ttu-id="ad71d-132">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad71d-133">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="ad71d-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-134">-게이트웨이 Sku</span><span class="sxs-lookup"><span data-stu-id="ad71d-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-135">-게이트웨이 종류</span><span class="sxs-lookup"><span data-stu-id="ad71d-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="ad71d-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-137">-위치</span><span class="sxs-lookup"><span data-stu-id="ad71d-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-138">-이름</span><span class="sxs-lookup"><span data-stu-id="ad71d-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="ad71d-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="ad71d-140">-RadiusServerAddress</span></span>
<span data-ttu-id="ad71d-141">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="ad71d-142">-RadiusServerSecret</span></span>
<span data-ttu-id="ad71d-143">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="ad71d-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad71d-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-145">태그</span><span class="sxs-lookup"><span data-stu-id="ad71d-145">-Tag</span></span>
<span data-ttu-id="ad71d-146">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ad71d-147">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ad71d-147">For example:</span></span>

<span data-ttu-id="ad71d-148">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ad71d-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ad71d-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="ad71d-149">-VpnClientAddressPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="ad71d-150">-VpnClientProtocol</span></span>
<span data-ttu-id="ad71d-151">P2S VPN 클라이언트 터널링 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="ad71d-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="ad71d-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="ad71d-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="ad71d-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad71d-155">-확인</span><span class="sxs-lookup"><span data-stu-id="ad71d-155">-Confirm</span></span>
<span data-ttu-id="ad71d-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad71d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad71d-157">-WhatIf</span></span>
<span data-ttu-id="ad71d-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad71d-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad71d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad71d-160">CommonParameters</span></span>
<span data-ttu-id="ad71d-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad71d-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad71d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad71d-163">입력</span><span class="sxs-lookup"><span data-stu-id="ad71d-163">INPUTS</span></span>

### <span data-ttu-id="ad71d-164">않아야</span><span class="sxs-lookup"><span data-stu-id="ad71d-164">None</span></span>
<span data-ttu-id="ad71d-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad71d-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad71d-166">출력</span><span class="sxs-lookup"><span data-stu-id="ad71d-166">OUTPUTS</span></span>

### <span data-ttu-id="ad71d-167">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ad71d-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ad71d-168">상속자</span><span class="sxs-lookup"><span data-stu-id="ad71d-168">NOTES</span></span>

## <span data-ttu-id="ad71d-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad71d-169">RELATED LINKS</span></span>

[<span data-ttu-id="ad71d-170">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad71d-170">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ad71d-171">제거-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad71d-171">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ad71d-172">다시 설정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad71d-172">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ad71d-173">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad71d-173">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="ad71d-174">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ad71d-174">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
