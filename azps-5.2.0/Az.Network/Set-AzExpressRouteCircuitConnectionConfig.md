---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325898"
---
# <span data-ttu-id="0b1f5-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b1f5-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="0b1f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1f5-103">Express Route 회로에 대한 개인 피어링에서 만든 회로 연결 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="0b1f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b1f5-104">SYNTAX</span></span>

### <span data-ttu-id="0b1f5-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="0b1f5-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b1f5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b1f5-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b1f5-107">설명</span><span class="sxs-lookup"><span data-stu-id="0b1f5-107">DESCRIPTION</span></span>
<span data-ttu-id="0b1f5-108">**Set-AzExpressRouteCircuitConnectionConfig** cmdlet은 ExpressRoute 회로에 대한 개인 피어링에서 만든 회로 연결 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="0b1f5-109">이렇게 하면 지역 또는 구독에서 두 Express Route 회로를 피어링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="0b1f5-110">**Set-AzExpressRouteCircuitConnectionConfig를** 실행하기 전에 **Add-AzExpressRouteCircuitConnectionConfig를** 사용하여 회로 연결을 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="0b1f5-111">또한 **Set-AzExpressRouteCircuitPeeringConfig를** 실행한 후 Set-AzExpressRouteCircuit cmdlet을 호출하여 구성을 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="0b1f5-112">예제</span><span class="sxs-lookup"><span data-stu-id="0b1f5-112">EXAMPLES</span></span>

### <span data-ttu-id="0b1f5-113">예제 1: 기존 ExpressRoute 회로로 회로 연결 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="0b1f5-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="0b1f5-114">예제 2: 기존 ExpressRoute 회로에 파이핑을 사용하여 회로 연결 구성 설정</span><span class="sxs-lookup"><span data-stu-id="0b1f5-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="0b1f5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b1f5-115">PARAMETERS</span></span>

### <span data-ttu-id="0b1f5-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0b1f5-116">-AddressPrefix</span></span>
<span data-ttu-id="0b1f5-117">IPv4 터널에 대한 Express Route 회로 간에 VxLan 터널을 만드는 최소 /29개 고객 주소 공간입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="0b1f5-118">또는 IPv6 터널에 대한 Express Route 회로 간에 VxLan 터널을 만들 수 있는 최소 /125의 고객 주소 공간입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="0b1f5-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="0b1f5-119">-AddressPrefixType</span></span>
<span data-ttu-id="0b1f5-120">주소가 속한 주소 패밀리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f5-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="0b1f5-121">-AuthorizationKey</span></span>
<span data-ttu-id="0b1f5-122">다른 구독에서 Express Route 회로를 피어링하는 권한 부여 키입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="0b1f5-123">기존 명령을 사용하여 피어 회로에 대한 권한 부여를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="0b1f5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1f5-124">-DefaultProfile</span></span>
<span data-ttu-id="0b1f5-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b1f5-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b1f5-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0b1f5-127">수정되는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="0b1f5-128">**Get-AzExpressRouteCircuit** cmdlet에서 반환된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0b1f5-129">-Name</span></span>
<span data-ttu-id="0b1f5-130">추가할 회로 연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-130">The name of the circuit connection resource to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f5-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="0b1f5-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="0b1f5-132">현재 회로와 피어링될 원격 회로의 개인 피어링에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b1f5-133">-Confirm</span></span>
<span data-ttu-id="0b1f5-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b1f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b1f5-135">-WhatIf</span></span>
<span data-ttu-id="0b1f5-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0b1f5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b1f5-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b1f5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1f5-138">CommonParameters</span></span>
<span data-ttu-id="0b1f5-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1f5-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0b1f5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1f5-141">입력</span><span class="sxs-lookup"><span data-stu-id="0b1f5-141">INPUTS</span></span>

### <span data-ttu-id="0b1f5-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b1f5-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="0b1f5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0b1f5-143">System.String</span></span>

## <span data-ttu-id="0b1f5-144">출력</span><span class="sxs-lookup"><span data-stu-id="0b1f5-144">OUTPUTS</span></span>

### <span data-ttu-id="0b1f5-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b1f5-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0b1f5-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b1f5-146">NOTES</span></span>

## <span data-ttu-id="0b1f5-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b1f5-147">RELATED LINKS</span></span>

[<span data-ttu-id="0b1f5-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b1f5-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b1f5-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b1f5-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b1f5-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b1f5-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="0b1f5-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b1f5-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="0b1f5-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0b1f5-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
