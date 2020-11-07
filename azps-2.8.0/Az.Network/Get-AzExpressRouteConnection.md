---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 01b8c32af3edc6c10070bdbd61c7f84fa055af23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870202"
---
# <span data-ttu-id="cfb99-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cfb99-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="cfb99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfb99-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb99-103">ExpressRouteGateway에 연결 된 모든 Express 경로 연결을 이름 또는 이름별로 연결을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="cfb99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cfb99-104">SYNTAX</span></span>

### <span data-ttu-id="cfb99-105">ByExpressRouteGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="cfb99-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfb99-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cfb99-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfb99-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb99-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfb99-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cfb99-108">DESCRIPTION</span></span>
<span data-ttu-id="cfb99-109">ExpressRouteGateway에 연결 된 모든 Express 경로 연결을 이름 또는 이름별로 연결을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="cfb99-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cfb99-110">EXAMPLES</span></span>

### <span data-ttu-id="cfb99-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cfb99-111">Example 1</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="cfb99-112">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 ExpressRouteSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="cfb99-113">1 개의 배율 단위를 사용 하 여 가상 허브에 Express 경로 게이트웨이가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="cfb99-114">게이트웨이가 생성 되 면 New-AzExpressRouteConnection 명령을 사용 하 여 온-프레미스 Express 경로 회로에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="cfb99-115">그런 다음 연결 이름을 사용 하 여 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="cfb99-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="cfb99-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="cfb99-117">이 명령은 "test"로 시작 하는 Express 경로 "testExpressRoutegw"의 모든 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="cfb99-118">변수</span><span class="sxs-lookup"><span data-stu-id="cfb99-118">PARAMETERS</span></span>

### <span data-ttu-id="cfb99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb99-119">-DefaultProfile</span></span>
<span data-ttu-id="cfb99-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb99-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="cfb99-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="cfb99-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-122">The parent resource name.</span></span>

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

### <span data-ttu-id="cfb99-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cfb99-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="cfb99-124">이 연결에 대 한 부모 ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="cfb99-124">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="cfb99-125">-이름</span><span class="sxs-lookup"><span data-stu-id="cfb99-125">-Name</span></span>
<span data-ttu-id="cfb99-126">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="cfb99-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cfb99-127">-ParentResourceId</span></span>
<span data-ttu-id="cfb99-128">이 연결에 대 한 부모 ExpressRouteGateway의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="cfb99-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfb99-129">-ResourceGroupName</span></span>
<span data-ttu-id="cfb99-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-130">The resource group name.</span></span>

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

### <span data-ttu-id="cfb99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb99-131">CommonParameters</span></span>
<span data-ttu-id="cfb99-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cfb99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb99-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cfb99-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb99-134">입력</span><span class="sxs-lookup"><span data-stu-id="cfb99-134">INPUTS</span></span>

### <span data-ttu-id="cfb99-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cfb99-135">System.String</span></span>

## <span data-ttu-id="cfb99-136">출력</span><span class="sxs-lookup"><span data-stu-id="cfb99-136">OUTPUTS</span></span>

### <span data-ttu-id="cfb99-137">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cfb99-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="cfb99-138">상속자</span><span class="sxs-lookup"><span data-stu-id="cfb99-138">NOTES</span></span>

## <span data-ttu-id="cfb99-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfb99-139">RELATED LINKS</span></span>
