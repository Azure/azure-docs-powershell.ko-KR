---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366850"
---
# <span data-ttu-id="238a3-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="238a3-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="238a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238a3-102">SYNOPSIS</span></span>
<span data-ttu-id="238a3-103">ExpressRouteConnection을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="238a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="238a3-104">SYNTAX</span></span>

### <span data-ttu-id="238a3-105">ByExpressRouteConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="238a3-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238a3-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="238a3-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238a3-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="238a3-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="238a3-108">DESCRIPTION</span></span>
<span data-ttu-id="238a3-109">ExpressRouteConnection을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="238a3-110">예제</span><span class="sxs-lookup"><span data-stu-id="238a3-110">EXAMPLES</span></span>

### <span data-ttu-id="238a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="238a3-111">Example 1</span></span>
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
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="238a3-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="238a3-113">ExpressRoute 게이트웨이는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="238a3-114">게이트웨이가 만들어졌다면 다음 명령을 사용하여 ExpressRouteSite에 New-AzExpressRouteConnection 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="238a3-115">그런 다음 연결 이름을 사용하여 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="238a3-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="238a3-116">Example 2</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="238a3-117">예제 1과 동일하지만 이제 Get-AzExpressRouteConnection에서 파이프된 개체를 사용하여 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="238a3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="238a3-118">PARAMETERS</span></span>

### <span data-ttu-id="238a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238a3-119">-DefaultProfile</span></span>
<span data-ttu-id="238a3-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="238a3-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="238a3-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="238a3-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-122">The parent resource name.</span></span>

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

### <span data-ttu-id="238a3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="238a3-123">-Force</span></span>
<span data-ttu-id="238a3-124">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="238a3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="238a3-125">-InputObject</span></span>
<span data-ttu-id="238a3-126">업데이트할 ExpressRouteConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="238a3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="238a3-127">-Name</span></span>
<span data-ttu-id="238a3-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-128">The resource name.</span></span>

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

### <span data-ttu-id="238a3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="238a3-129">-PassThru</span></span>
<span data-ttu-id="238a3-130">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="238a3-131">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="238a3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238a3-132">-ResourceGroupName</span></span>
<span data-ttu-id="238a3-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-133">The resource group name.</span></span>

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

### <span data-ttu-id="238a3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="238a3-134">-ResourceId</span></span>
<span data-ttu-id="238a3-135">삭제할 ExpressRouteConnection 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="238a3-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="238a3-136">-Confirm</span></span>
<span data-ttu-id="238a3-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="238a3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="238a3-138">-WhatIf</span></span>
<span data-ttu-id="238a3-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="238a3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="238a3-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="238a3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238a3-141">CommonParameters</span></span>
<span data-ttu-id="238a3-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="238a3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238a3-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="238a3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238a3-144">입력</span><span class="sxs-lookup"><span data-stu-id="238a3-144">INPUTS</span></span>

### <span data-ttu-id="238a3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="238a3-145">System.String</span></span>

### <span data-ttu-id="238a3-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="238a3-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="238a3-147">출력</span><span class="sxs-lookup"><span data-stu-id="238a3-147">OUTPUTS</span></span>

### <span data-ttu-id="238a3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="238a3-148">System.Boolean</span></span>

## <span data-ttu-id="238a3-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="238a3-149">NOTES</span></span>

## <span data-ttu-id="238a3-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="238a3-150">RELATED LINKS</span></span>
