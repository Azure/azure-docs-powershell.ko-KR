---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 72aa8af012addf4fa309adc7c63467ecaf667fff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700353"
---
# <span data-ttu-id="15a64-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="15a64-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="15a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a64-102">SYNOPSIS</span></span>
<span data-ttu-id="15a64-103">이 (가) 구내 게이트웨이를 온-프레미스 Express 경로 회로에 연결 하는 Express 경로 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="15a64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15a64-104">SYNTAX</span></span>

### <span data-ttu-id="15a64-105">ByExpressRouteGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="15a64-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a64-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="15a64-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a64-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="15a64-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a64-108">설명은</span><span class="sxs-lookup"><span data-stu-id="15a64-108">DESCRIPTION</span></span>
<span data-ttu-id="15a64-109">가상 허브 내의 Express 경로 게이트웨이로의 온-프레미스 대상 경로 회로 BGP 피어 링 간의 Express 경로 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="15a64-110">예제의</span><span class="sxs-lookup"><span data-stu-id="15a64-110">EXAMPLES</span></span>

### <span data-ttu-id="15a64-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="15a64-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="15a64-112">위의 방법에서는 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 사설 피어 링을 사용 하 여 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브, Express 라우팅 게이트웨이 및 Express 경로를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="15a64-113">게이트웨이가 만들어졌으면 New-AzExpressRouteConnection 명령을 사용 하 여 Express 경로 링에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="15a64-114">변수</span><span class="sxs-lookup"><span data-stu-id="15a64-114">PARAMETERS</span></span>

### <span data-ttu-id="15a64-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15a64-115">-AsJob</span></span>
<span data-ttu-id="15a64-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="15a64-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15a64-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="15a64-117">-AuthorizationKey</span></span>
<span data-ttu-id="15a64-118">다른 구독에서 게이트웨이와 연결을 만들 수 있도록이 경로를 사용 하 여 Express 회로 소유자 로부터 받은 키입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="15a64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a64-119">-DefaultProfile</span></span>
<span data-ttu-id="15a64-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a64-121">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="15a64-121">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="15a64-122">이 Express Route gateway 연결을 만들 Express 경로 회로 피어 링의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-122">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="15a64-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="15a64-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="15a64-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a64-125">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="15a64-125">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="15a64-126">이 연결에 대 한 부모 ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="15a64-126">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a64-127">-이름</span><span class="sxs-lookup"><span data-stu-id="15a64-127">-Name</span></span>
<span data-ttu-id="15a64-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a64-129">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15a64-129">-ParentResourceId</span></span>
<span data-ttu-id="15a64-130">이 연결에 대 한 부모 ExpressRouteGateway의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-130">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a64-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a64-131">-ResourceGroupName</span></span>
<span data-ttu-id="15a64-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a64-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="15a64-133">-RoutingWeight</span></span>
<span data-ttu-id="15a64-134">이 연결에 할당 해야 하는 패킷 라우팅의 중량입니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-134">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a64-135">-확인</span><span class="sxs-lookup"><span data-stu-id="15a64-135">-Confirm</span></span>
<span data-ttu-id="15a64-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a64-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a64-137">-WhatIf</span></span>
<span data-ttu-id="15a64-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a64-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a64-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a64-140">CommonParameters</span></span>
<span data-ttu-id="15a64-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a64-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a64-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a64-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a64-143">입력</span><span class="sxs-lookup"><span data-stu-id="15a64-143">INPUTS</span></span>

### <span data-ttu-id="15a64-144">PSExpressRouteGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15a64-144">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="15a64-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15a64-145">System.String</span></span>

## <span data-ttu-id="15a64-146">출력</span><span class="sxs-lookup"><span data-stu-id="15a64-146">OUTPUTS</span></span>

### <span data-ttu-id="15a64-147">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15a64-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="15a64-148">상속자</span><span class="sxs-lookup"><span data-stu-id="15a64-148">NOTES</span></span>

## <span data-ttu-id="15a64-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15a64-149">RELATED LINKS</span></span>
