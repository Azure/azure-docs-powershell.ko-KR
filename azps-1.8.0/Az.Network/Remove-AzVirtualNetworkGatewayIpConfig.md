---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 9c36025f6de4ef6e6168bf5578d09d577cc4f46b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700101"
---
# <span data-ttu-id="7359f-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7359f-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7359f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7359f-102">SYNOPSIS</span></span>
<span data-ttu-id="7359f-103">가상 네트워크 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="7359f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7359f-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7359f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7359f-105">DESCRIPTION</span></span>
<span data-ttu-id="7359f-106">가상 네트워크 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="7359f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7359f-107">EXAMPLES</span></span>

### <span data-ttu-id="7359f-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="7359f-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="7359f-109">변수</span><span class="sxs-lookup"><span data-stu-id="7359f-109">PARAMETERS</span></span>

### <span data-ttu-id="7359f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7359f-110">-DefaultProfile</span></span>
<span data-ttu-id="7359f-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7359f-112">-이름</span><span class="sxs-lookup"><span data-stu-id="7359f-112">-Name</span></span>
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

### <span data-ttu-id="7359f-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7359f-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="7359f-114">-확인</span><span class="sxs-lookup"><span data-stu-id="7359f-114">-Confirm</span></span>
<span data-ttu-id="7359f-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7359f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7359f-116">-WhatIf</span></span>
<span data-ttu-id="7359f-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7359f-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7359f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7359f-119">CommonParameters</span></span>
<span data-ttu-id="7359f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7359f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7359f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7359f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7359f-122">입력</span><span class="sxs-lookup"><span data-stu-id="7359f-122">INPUTS</span></span>

### <span data-ttu-id="7359f-123">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7359f-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7359f-124">출력</span><span class="sxs-lookup"><span data-stu-id="7359f-124">OUTPUTS</span></span>

### <span data-ttu-id="7359f-125">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7359f-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7359f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="7359f-126">NOTES</span></span>

## <span data-ttu-id="7359f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7359f-127">RELATED LINKS</span></span>

[<span data-ttu-id="7359f-128">추가-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7359f-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="7359f-129">새로운 AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7359f-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
