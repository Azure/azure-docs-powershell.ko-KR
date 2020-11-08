---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: dc3cde19bde2da95fd2ffc731223783c1963d1f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218517"
---
# <span data-ttu-id="e7c95-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e7c95-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="e7c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7c95-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c95-103">Express 경로 게이트웨이와 온-프레미스 express 경로 회로 피어 링 간에 생성 된 express 경로 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="e7c95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7c95-104">SYNTAX</span></span>

### <span data-ttu-id="e7c95-105">ByExpressRouteConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7c95-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7c95-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e7c95-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7c95-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e7c95-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7c95-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e7c95-108">DESCRIPTION</span></span>
<span data-ttu-id="e7c95-109">**AzExpressRouteConnection** cmdlet은 express 경로 게이트웨이와 온-프레미스 express 경로 회로 피어 링 간에 생성 되는 express 경로 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="e7c95-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e7c95-110">EXAMPLES</span></span>

### <span data-ttu-id="e7c95-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7c95-111">Example 1</span></span>

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

<span data-ttu-id="e7c95-112">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 ExpressRouteSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e7c95-113">1 개의 배율 단위를 사용 하 여 가상 허브에 Express 경로 게이트웨이가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e7c95-114">게이트웨이가 생성 되 면 New-AzExpressRouteConnection 명령을 사용 하 여 온-프레미스 Express 경로 회로 피어 링에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="e7c95-115">그런 다음 Set-AzExpressRouteConnection 명령을 사용 하 여 다른 RoutingWeight를 포함 하도록 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="e7c95-116">변수</span><span class="sxs-lookup"><span data-stu-id="e7c95-116">PARAMETERS</span></span>

### <span data-ttu-id="e7c95-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7c95-117">-AsJob</span></span>
<span data-ttu-id="e7c95-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e7c95-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7c95-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="e7c95-119">-AuthorizationKey</span></span>
<span data-ttu-id="e7c95-120">Express 경로 게이트웨이 연결을 만드는 데 사용할 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="e7c95-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c95-121">-DefaultProfile</span></span>
<span data-ttu-id="e7c95-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7c95-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="e7c95-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="e7c95-124">이 Express 게이트웨이 연결에 인터넷 보안 사용</span><span class="sxs-lookup"><span data-stu-id="e7c95-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="e7c95-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="e7c95-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="e7c95-126">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-126">The parent resource name.</span></span>

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

### <span data-ttu-id="e7c95-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7c95-127">-InputObject</span></span>
<span data-ttu-id="e7c95-128">업데이트할 ExpressRouteConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-128">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="e7c95-129">-이름</span><span class="sxs-lookup"><span data-stu-id="e7c95-129">-Name</span></span>
<span data-ttu-id="e7c95-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-130">The resource name.</span></span>

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

### <span data-ttu-id="e7c95-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c95-131">-ResourceGroupName</span></span>
<span data-ttu-id="e7c95-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-132">The resource group name.</span></span>

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

### <span data-ttu-id="e7c95-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7c95-133">-ResourceId</span></span>
<span data-ttu-id="e7c95-134">삭제할 ExpressRouteConnection 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="e7c95-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c95-135">-RoutingConfiguration</span></span>
<span data-ttu-id="e7c95-136">이 연결에 대 한 라우팅 구성</span><span class="sxs-lookup"><span data-stu-id="e7c95-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="e7c95-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="e7c95-137">-RoutingWeight</span></span>
<span data-ttu-id="e7c95-138">패킷 라우팅에 대해이 연결에 할당 해야 하는 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-138">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="e7c95-139">-확인</span><span class="sxs-lookup"><span data-stu-id="e7c95-139">-Confirm</span></span>
<span data-ttu-id="e7c95-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7c95-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c95-141">-WhatIf</span></span>
<span data-ttu-id="e7c95-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c95-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7c95-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c95-144">CommonParameters</span></span>
<span data-ttu-id="e7c95-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7c95-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c95-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7c95-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c95-147">입력</span><span class="sxs-lookup"><span data-stu-id="e7c95-147">INPUTS</span></span>

### <span data-ttu-id="e7c95-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e7c95-148">System.String</span></span>

### <span data-ttu-id="e7c95-149">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e7c95-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="e7c95-150">출력</span><span class="sxs-lookup"><span data-stu-id="e7c95-150">OUTPUTS</span></span>

### <span data-ttu-id="e7c95-151">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e7c95-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="e7c95-152">상속자</span><span class="sxs-lookup"><span data-stu-id="e7c95-152">NOTES</span></span>

## <span data-ttu-id="e7c95-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7c95-153">RELATED LINKS</span></span>

[<span data-ttu-id="e7c95-154">새로운 AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7c95-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
