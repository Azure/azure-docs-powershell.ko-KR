---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179468"
---
# <span data-ttu-id="a35b2-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a35b2-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="a35b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a35b2-103">Virtual Network 게이트웨이에서 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a35b2-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="a35b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="a35b2-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a35b2-105">설명</span><span class="sxs-lookup"><span data-stu-id="a35b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a35b2-106">Virtual Network 게이트웨이에서 IP 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a35b2-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="a35b2-107">예제</span><span class="sxs-lookup"><span data-stu-id="a35b2-107">EXAMPLES</span></span>

### <span data-ttu-id="a35b2-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="a35b2-108">Example 1:</span></span>
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

## <span data-ttu-id="a35b2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a35b2-109">PARAMETERS</span></span>

### <span data-ttu-id="a35b2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35b2-110">-DefaultProfile</span></span>
<span data-ttu-id="a35b2-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a35b2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a35b2-112">-Name</span><span class="sxs-lookup"><span data-stu-id="a35b2-112">-Name</span></span>
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

### <span data-ttu-id="a35b2-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a35b2-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="a35b2-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a35b2-114">-Confirm</span></span>
<span data-ttu-id="a35b2-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a35b2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a35b2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a35b2-116">-WhatIf</span></span>
<span data-ttu-id="a35b2-117">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a35b2-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a35b2-118">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a35b2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a35b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35b2-119">CommonParameters</span></span>
<span data-ttu-id="a35b2-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a35b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35b2-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a35b2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35b2-122">입력</span><span class="sxs-lookup"><span data-stu-id="a35b2-122">INPUTS</span></span>

### <span data-ttu-id="a35b2-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a35b2-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a35b2-124">출력</span><span class="sxs-lookup"><span data-stu-id="a35b2-124">OUTPUTS</span></span>

### <span data-ttu-id="a35b2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a35b2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a35b2-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a35b2-126">NOTES</span></span>

## <span data-ttu-id="a35b2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a35b2-127">RELATED LINKS</span></span>

[<span data-ttu-id="a35b2-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a35b2-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="a35b2-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a35b2-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
