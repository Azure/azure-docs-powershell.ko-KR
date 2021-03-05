---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: ad31bd55c86a785ce45a7f2ca43a20f5a1a97c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964048"
---
# <span data-ttu-id="8e0de-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e0de-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="8e0de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e0de-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0de-103">Express 경로 게이트웨이와 프레미스 익스프레스 경로 회로 피어링 간에 생성된 익스프레스 경로 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8e0de-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e0de-104">SYNTAX</span></span>

### <span data-ttu-id="8e0de-105">ByExpressRouteConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8e0de-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0de-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="8e0de-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e0de-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8e0de-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e0de-108">설명</span><span class="sxs-lookup"><span data-stu-id="8e0de-108">DESCRIPTION</span></span>
<span data-ttu-id="8e0de-109">**Set-AzExpressRouteConnection** cmdlet은 익스프레스 경로 게이트웨이와 프레미스 익스프레스 경로 회로 피어링 간에 생성된 익스프레스 경로 연결을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8e0de-110">예제</span><span class="sxs-lookup"><span data-stu-id="8e0de-110">EXAMPLES</span></span>

### <span data-ttu-id="8e0de-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e0de-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
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

<span data-ttu-id="8e0de-112">위의 리소스 그룹, Virtual WAN, Virtual Network, Virtual Hub 및 ExpressRouteSite는 Azure의 "testRG" 리소스 그룹에서 미국 서부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8e0de-113">2개 확장 단위가 있는 Virtual Hub에서 ExpressRoute 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8e0de-114">게이트웨이를 만든 후 이 게이트웨이는 New-AzExpressRouteConnection 사용하여 프레미스 ExpressRoute 회로 피어링에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="8e0de-115">그런 다음, 연결은 Set-AzExpressRouteConnection 사용하여 다른 RoutingWeight를 Set-AzExpressRouteConnection 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="8e0de-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e0de-116">PARAMETERS</span></span>

### <span data-ttu-id="8e0de-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e0de-117">-AsJob</span></span>
<span data-ttu-id="8e0de-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8e0de-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e0de-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="8e0de-119">-AuthorizationKey</span></span>
<span data-ttu-id="8e0de-120">ExpressRoute 게이트웨이 연결을 만드는 데 사용할 권한 부여 키입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="8e0de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0de-121">-DefaultProfile</span></span>
<span data-ttu-id="8e0de-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e0de-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8e0de-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="8e0de-124">이 ExpressRoute Gateway 연결에 대한 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="8e0de-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="8e0de-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="8e0de-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="8e0de-126">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0de-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e0de-127">-InputObject</span></span>
<span data-ttu-id="8e0de-128">업데이트할 ExpressRouteConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0de-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8e0de-129">-Name</span></span>
<span data-ttu-id="8e0de-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0de-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e0de-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e0de-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0de-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e0de-133">-ResourceId</span></span>
<span data-ttu-id="8e0de-134">삭제할 ExpressRouteConnection 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0de-135">-라우팅Configuration</span><span class="sxs-lookup"><span data-stu-id="8e0de-135">-RoutingConfiguration</span></span>
<span data-ttu-id="8e0de-136">이 연결에 대한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="8e0de-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="8e0de-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="8e0de-137">-RoutingWeight</span></span>
<span data-ttu-id="8e0de-138">패킷 라우팅을 위해 이 연결에 할당해야 하는 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-138">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="8e0de-139">-확인</span><span class="sxs-lookup"><span data-stu-id="8e0de-139">-Confirm</span></span>
<span data-ttu-id="8e0de-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e0de-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e0de-141">-WhatIf</span></span>
<span data-ttu-id="8e0de-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e0de-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e0de-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0de-144">CommonParameters</span></span>
<span data-ttu-id="8e0de-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e0de-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0de-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e0de-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0de-147">입력</span><span class="sxs-lookup"><span data-stu-id="8e0de-147">INPUTS</span></span>

### <span data-ttu-id="8e0de-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8e0de-148">System.String</span></span>

### <span data-ttu-id="8e0de-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e0de-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8e0de-150">출력</span><span class="sxs-lookup"><span data-stu-id="8e0de-150">OUTPUTS</span></span>

### <span data-ttu-id="8e0de-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8e0de-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8e0de-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e0de-152">NOTES</span></span>

## <span data-ttu-id="8e0de-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e0de-153">RELATED LINKS</span></span>

[<span data-ttu-id="8e0de-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e0de-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
