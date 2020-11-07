---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 7a5b06f41d7cf616716d3450e06689cd657b8190
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871090"
---
# <span data-ttu-id="37ede-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="37ede-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="37ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ede-102">SYNOPSIS</span></span>
<span data-ttu-id="37ede-103">Express 경로 게이트웨이와 온-프레미스 express 경로 회로 피어 링 간에 생성 된 express 경로 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="37ede-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37ede-104">SYNTAX</span></span>

### <span data-ttu-id="37ede-105">ByExpressRouteConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="37ede-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ede-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="37ede-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ede-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="37ede-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37ede-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37ede-108">DESCRIPTION</span></span>
<span data-ttu-id="37ede-109">**AzExpressRouteConnection** cmdlet은 express 경로 게이트웨이와 온-프레미스 express 경로 회로 피어 링 간에 생성 되는 express 경로 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="37ede-110">예제의</span><span class="sxs-lookup"><span data-stu-id="37ede-110">EXAMPLES</span></span>

### <span data-ttu-id="37ede-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="37ede-111">Example 1</span></span>

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
```

<span data-ttu-id="37ede-112">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 ExpressRouteSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="37ede-113">1 개의 배율 단위를 사용 하 여 가상 허브에 Express 경로 게이트웨이가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="37ede-114">게이트웨이가 생성 되 면 New-AzExpressRouteConnection 명령을 사용 하 여 온-프레미스 Express 경로 회로 피어 링에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="37ede-115">그런 다음 Set-AzExpressRouteConnection 명령을 사용 하 여 다른 RoutingWeight를 포함 하도록 연결을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="37ede-116">변수</span><span class="sxs-lookup"><span data-stu-id="37ede-116">PARAMETERS</span></span>

### <span data-ttu-id="37ede-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37ede-117">-AsJob</span></span>
<span data-ttu-id="37ede-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="37ede-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37ede-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="37ede-119">-AuthorizationKey</span></span>
<span data-ttu-id="37ede-120">Express 경로 게이트웨이 연결을 만드는 데 사용할 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="37ede-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ede-121">-DefaultProfile</span></span>
<span data-ttu-id="37ede-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ede-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="37ede-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="37ede-124">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37ede-125">-InputObject</span></span>
<span data-ttu-id="37ede-126">업데이트할 ExpressRouteConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-127">-이름</span><span class="sxs-lookup"><span data-stu-id="37ede-127">-Name</span></span>
<span data-ttu-id="37ede-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ede-129">-ResourceGroupName</span></span>
<span data-ttu-id="37ede-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37ede-131">-ResourceId</span></span>
<span data-ttu-id="37ede-132">삭제할 ExpressRouteConnection 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-132">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ede-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="37ede-133">-RoutingWeight</span></span>
<span data-ttu-id="37ede-134">패킷 라우팅에 대해이 연결에 할당 해야 하는 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-134">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="37ede-135">-확인</span><span class="sxs-lookup"><span data-stu-id="37ede-135">-Confirm</span></span>
<span data-ttu-id="37ede-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ede-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ede-137">-WhatIf</span></span>
<span data-ttu-id="37ede-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ede-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ede-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ede-140">CommonParameters</span></span>
<span data-ttu-id="37ede-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37ede-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ede-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ede-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ede-143">입력</span><span class="sxs-lookup"><span data-stu-id="37ede-143">INPUTS</span></span>

### <span data-ttu-id="37ede-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37ede-144">System.String</span></span>

### <span data-ttu-id="37ede-145">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="37ede-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="37ede-146">출력</span><span class="sxs-lookup"><span data-stu-id="37ede-146">OUTPUTS</span></span>

### <span data-ttu-id="37ede-147">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="37ede-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="37ede-148">상속자</span><span class="sxs-lookup"><span data-stu-id="37ede-148">NOTES</span></span>

## <span data-ttu-id="37ede-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37ede-149">RELATED LINKS</span></span>
