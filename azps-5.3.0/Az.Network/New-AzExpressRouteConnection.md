---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385505"
---
# <span data-ttu-id="ae4ec-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ae4ec-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="ae4ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4ec-103">ExpressRoute 게이트웨이를 프레미스 ExpressRoute 회로에 연결하는 ExpressRoute 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="ae4ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae4ec-104">SYNTAX</span></span>

### <span data-ttu-id="ae4ec-105">ByExpressRouteGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae4ec-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae4ec-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ae4ec-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae4ec-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ae4ec-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4ec-108">설명</span><span class="sxs-lookup"><span data-stu-id="ae4ec-108">DESCRIPTION</span></span>
<span data-ttu-id="ae4ec-109">가상 허브 내부의 ExpressRoute 게이트웨이에 대한 BGP 피어링과의 ExpressRoute 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="ae4ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="ae4ec-110">EXAMPLES</span></span>

### <span data-ttu-id="ae4ec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae4ec-111">Example 1</span></span>

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
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="ae4ec-112">위에서는 Azure의 "testRG" 리소스 그룹에 미국 중서부에 개인 피어링이 있는 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub, ExpressRoute 게이트웨이 및 ExpressRoute 회로를 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="ae4ec-113">게이트웨이를 만든 후 게이트웨이는 New-AzExpressRouteConnection 사용하여 ExpressRoute 회로 피어링에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="ae4ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4ec-114">PARAMETERS</span></span>

### <span data-ttu-id="ae4ec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae4ec-115">-AsJob</span></span>
<span data-ttu-id="ae4ec-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ae4ec-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae4ec-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="ae4ec-117">-AuthorizationKey</span></span>
<span data-ttu-id="ae4ec-118">ExpressRoute 회로 소유자가 다른 구독의 게이트웨이와 연결을 만들 수 있는 키입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4ec-119">-DefaultProfile</span></span>
<span data-ttu-id="ae4ec-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="ae4ec-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="ae4ec-122">이 ExpressRoute 게이트웨이 연결에 대한 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="ae4ec-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="ae4ec-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="ae4ec-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="ae4ec-124">이 Express Route 게이트웨이 연결을 만들 Express Route 회로 피어링의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="ae4ec-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="ae4ec-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ae4ec-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="ae4ec-128">이 연결에 대한 상위 ExpressRouteGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ae4ec-129">-Name</span></span>
<span data-ttu-id="ae4ec-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ae4ec-131">-ParentResourceId</span></span>
<span data-ttu-id="ae4ec-132">이 연결에 대한 상위 ExpressRouteGateway의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4ec-133">-ResourceGroupName</span></span>
<span data-ttu-id="ae4ec-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae4ec-135">-RoutingConfiguration</span></span>
<span data-ttu-id="ae4ec-136">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="ae4ec-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="ae4ec-137">-RoutingWeight</span></span>
<span data-ttu-id="ae4ec-138">이 연결에 할당해야 하는 패킷 라우팅의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae4ec-139">-Confirm</span></span>
<span data-ttu-id="ae4ec-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4ec-141">-WhatIf</span></span>
<span data-ttu-id="ae4ec-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ae4ec-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4ec-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4ec-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4ec-144">CommonParameters</span></span>
<span data-ttu-id="ae4ec-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4ec-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae4ec-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4ec-147">입력</span><span class="sxs-lookup"><span data-stu-id="ae4ec-147">INPUTS</span></span>

### <span data-ttu-id="ae4ec-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="ae4ec-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="ae4ec-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ae4ec-149">System.String</span></span>

## <span data-ttu-id="ae4ec-150">출력</span><span class="sxs-lookup"><span data-stu-id="ae4ec-150">OUTPUTS</span></span>

### <span data-ttu-id="ae4ec-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="ae4ec-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="ae4ec-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae4ec-152">NOTES</span></span>

## <span data-ttu-id="ae4ec-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae4ec-153">RELATED LINKS</span></span>

[<span data-ttu-id="ae4ec-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae4ec-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
