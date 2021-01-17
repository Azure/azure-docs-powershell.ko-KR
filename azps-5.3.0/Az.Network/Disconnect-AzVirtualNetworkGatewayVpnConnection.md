---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385645"
---
# <span data-ttu-id="44925-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="44925-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="44925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44925-102">SYNOPSIS</span></span> 
<span data-ttu-id="44925-103">주어진 가상 네트워크 게이트웨이를 사용하여 연결된 VPN 클라이언트 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="44925-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="44925-104">구문</span><span class="sxs-lookup"><span data-stu-id="44925-104">SYNTAX</span></span>
### <span data-ttu-id="44925-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="44925-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="44925-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="44925-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="44925-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="44925-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="44925-108">설명</span><span class="sxs-lookup"><span data-stu-id="44925-108">DESCRIPTION</span></span>
<span data-ttu-id="44925-109">**Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet을 사용하면 연결된 VPN 클라이언트 연결의 연결을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44925-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="44925-110">예제</span><span class="sxs-lookup"><span data-stu-id="44925-110">EXAMPLES</span></span>

### <span data-ttu-id="44925-111">예제</span><span class="sxs-lookup"><span data-stu-id="44925-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="44925-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44925-112">PARAMETERS</span></span>

### <span data-ttu-id="44925-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44925-113">-ResourceGroupName</span></span>
<span data-ttu-id="44925-114">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="44925-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44925-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="44925-115">-ResourceName</span></span>
<span data-ttu-id="44925-116">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="44925-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44925-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44925-117">-ResourceId</span></span>
<span data-ttu-id="44925-118">가상 네트워크 게이트웨이 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="44925-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44925-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="44925-119">-VpnConnectionId</span></span>
<span data-ttu-id="44925-120">Vpn 연결 ID</span><span class="sxs-lookup"><span data-stu-id="44925-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44925-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44925-121">-InputObject</span></span>
<span data-ttu-id="44925-122">가상 네트워크 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="44925-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44925-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44925-123">-AsJob</span></span>
<span data-ttu-id="44925-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="44925-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44925-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44925-125">CommonParameters</span></span>
<span data-ttu-id="44925-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44925-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44925-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44925-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44925-128">입력</span><span class="sxs-lookup"><span data-stu-id="44925-128">INPUTS</span></span>

### <span data-ttu-id="44925-129">System.String</span><span class="sxs-lookup"><span data-stu-id="44925-129">System.String</span></span>

## <span data-ttu-id="44925-130">출력</span><span class="sxs-lookup"><span data-stu-id="44925-130">OUTPUTS</span></span>

### <span data-ttu-id="44925-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="44925-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="44925-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44925-132">NOTES</span></span>

## <span data-ttu-id="44925-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44925-133">RELATED LINKS</span></span>
