---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: a0369a598cd7a3a0fa4044a267568260fbfda86c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870825"
---
# <span data-ttu-id="541bf-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="541bf-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="541bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="541bf-102">SYNOPSIS</span></span>
<span data-ttu-id="541bf-103">가상 네트워크 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="541bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="541bf-104">SYNTAX</span></span>

### <span data-ttu-id="541bf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="541bf-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="541bf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="541bf-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="541bf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="541bf-107">DESCRIPTION</span></span>
<span data-ttu-id="541bf-108">**Add-AzVirtualNetworkGatewayIpConfig** cmdlet은 가상 네트워크 게이트웨이에 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="541bf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="541bf-109">EXAMPLES</span></span>

### <span data-ttu-id="541bf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="541bf-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="541bf-111">변수</span><span class="sxs-lookup"><span data-stu-id="541bf-111">PARAMETERS</span></span>

### <span data-ttu-id="541bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="541bf-112">-DefaultProfile</span></span>
<span data-ttu-id="541bf-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="541bf-114">-이름</span><span class="sxs-lookup"><span data-stu-id="541bf-114">-Name</span></span>
<span data-ttu-id="541bf-115">추가할 게이트웨이 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="541bf-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="541bf-116">-PrivateIpAddress</span></span>
<span data-ttu-id="541bf-117">개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="541bf-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="541bf-118">-PublicIpAddress</span></span>
<span data-ttu-id="541bf-119">공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="541bf-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="541bf-120">-PublicIpAddressId</span></span>
<span data-ttu-id="541bf-121">공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="541bf-122">-서브넷</span><span class="sxs-lookup"><span data-stu-id="541bf-122">-Subnet</span></span>
<span data-ttu-id="541bf-123">**Pssubnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="541bf-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="541bf-124">-SubnetId</span></span>
<span data-ttu-id="541bf-125">서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="541bf-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="541bf-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="541bf-127">**PSVirtualNetworkGateway** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="541bf-128">이 cmdlet은 사용자가 지정 하는 **PSVirtualNetworkGateway** 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="541bf-129">Get-AzVirtualNetworkGateway cmdlet을 사용 하 여 **PSVirtualNetworkGateway** 개체를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="541bf-130">-확인</span><span class="sxs-lookup"><span data-stu-id="541bf-130">-Confirm</span></span>
<span data-ttu-id="541bf-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="541bf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="541bf-132">-WhatIf</span></span>
<span data-ttu-id="541bf-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="541bf-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="541bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="541bf-135">CommonParameters</span></span>
<span data-ttu-id="541bf-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="541bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="541bf-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="541bf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="541bf-138">입력</span><span class="sxs-lookup"><span data-stu-id="541bf-138">INPUTS</span></span>

### <span data-ttu-id="541bf-139">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="541bf-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="541bf-140">출력</span><span class="sxs-lookup"><span data-stu-id="541bf-140">OUTPUTS</span></span>

### <span data-ttu-id="541bf-141">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="541bf-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="541bf-142">상속자</span><span class="sxs-lookup"><span data-stu-id="541bf-142">NOTES</span></span>

## <span data-ttu-id="541bf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="541bf-143">RELATED LINKS</span></span>

[<span data-ttu-id="541bf-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="541bf-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="541bf-145">새로운 AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="541bf-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="541bf-146">제거-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="541bf-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
