---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 324999280df465a6fad621b6c4892e02cdd6e106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218518"
---
# <span data-ttu-id="58c2b-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="58c2b-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="58c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="58c2b-103">ExpressRouteConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="58c2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58c2b-104">SYNTAX</span></span>

### <span data-ttu-id="58c2b-105">ByExpressRouteConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="58c2b-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58c2b-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="58c2b-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58c2b-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="58c2b-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c2b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="58c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="58c2b-109">ExpressRouteConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="58c2b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="58c2b-110">EXAMPLES</span></span>

### <span data-ttu-id="58c2b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="58c2b-111">Example 1</span></span>
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

<span data-ttu-id="58c2b-112">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="58c2b-113">1 개의 배율 단위를 사용 하 여 가상 허브에 Express 경로 게이트웨이가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="58c2b-114">게이트웨이가 만들어지면 New-AzExpressRouteConnection 명령을 사용 하 여 ExpressRouteSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="58c2b-115">그런 다음 연결 이름을 사용 하 여 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="58c2b-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="58c2b-116">Example 2</span></span>

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

<span data-ttu-id="58c2b-117">예제 1과 동일 하지만 이제 AzExpressRouteConnection에서 파이핑 된 개체를 사용 하 여 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="58c2b-118">변수</span><span class="sxs-lookup"><span data-stu-id="58c2b-118">PARAMETERS</span></span>

### <span data-ttu-id="58c2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c2b-119">-DefaultProfile</span></span>
<span data-ttu-id="58c2b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c2b-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="58c2b-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="58c2b-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-122">The parent resource name.</span></span>

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

### <span data-ttu-id="58c2b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="58c2b-123">-Force</span></span>
<span data-ttu-id="58c2b-124">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="58c2b-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="58c2b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58c2b-125">-InputObject</span></span>
<span data-ttu-id="58c2b-126">업데이트할 ExpressRouteConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-126">The ExpressRouteConnection object to update.</span></span>

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

### <span data-ttu-id="58c2b-127">-이름</span><span class="sxs-lookup"><span data-stu-id="58c2b-127">-Name</span></span>
<span data-ttu-id="58c2b-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-128">The resource name.</span></span>

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

### <span data-ttu-id="58c2b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58c2b-129">-PassThru</span></span>
<span data-ttu-id="58c2b-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58c2b-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58c2b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c2b-132">-ResourceGroupName</span></span>
<span data-ttu-id="58c2b-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-133">The resource group name.</span></span>

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

### <span data-ttu-id="58c2b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58c2b-134">-ResourceId</span></span>
<span data-ttu-id="58c2b-135">삭제할 ExpressRouteConnection 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

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

### <span data-ttu-id="58c2b-136">-확인</span><span class="sxs-lookup"><span data-stu-id="58c2b-136">-Confirm</span></span>
<span data-ttu-id="58c2b-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c2b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c2b-138">-WhatIf</span></span>
<span data-ttu-id="58c2b-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c2b-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c2b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c2b-141">CommonParameters</span></span>
<span data-ttu-id="58c2b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58c2b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c2b-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c2b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c2b-144">입력</span><span class="sxs-lookup"><span data-stu-id="58c2b-144">INPUTS</span></span>

### <span data-ttu-id="58c2b-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58c2b-145">System.String</span></span>

### <span data-ttu-id="58c2b-146">PSExpressRouteConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="58c2b-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="58c2b-147">출력</span><span class="sxs-lookup"><span data-stu-id="58c2b-147">OUTPUTS</span></span>

### <span data-ttu-id="58c2b-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="58c2b-148">System.Boolean</span></span>

## <span data-ttu-id="58c2b-149">상속자</span><span class="sxs-lookup"><span data-stu-id="58c2b-149">NOTES</span></span>

## <span data-ttu-id="58c2b-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58c2b-150">RELATED LINKS</span></span>
