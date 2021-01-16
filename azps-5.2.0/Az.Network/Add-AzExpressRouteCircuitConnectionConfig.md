---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356138"
---
# <span data-ttu-id="2955f-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2955f-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="2955f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2955f-102">SYNOPSIS</span></span>
<span data-ttu-id="2955f-103">Express Route 회로의 개인 피어링에 회로 연결 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="2955f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2955f-104">SYNTAX</span></span>

### <span data-ttu-id="2955f-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="2955f-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2955f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2955f-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2955f-107">설명</span><span class="sxs-lookup"><span data-stu-id="2955f-107">DESCRIPTION</span></span>
<span data-ttu-id="2955f-108">**Add-AzExpressRouteCircuitConnectionConfig** cmdlet은 ExpressRoute 회로에 대한 개인 피어링에 회로 연결 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="2955f-109">이렇게 하면 지역 또는 구독에서 두 Express Route 회로를 피어링할 수 있습니다. **Add-AzExpressRouteCircuitConnectionConfig를** 실행한 후 Set-AzExpressRouteCircuit cmdlet을 호출하여 구성을 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="2955f-110">예제</span><span class="sxs-lookup"><span data-stu-id="2955f-110">EXAMPLES</span></span>

### <span data-ttu-id="2955f-111">예제 1: 기존 ExpressRoute 회로에 회로 연결 리소스 추가</span><span class="sxs-lookup"><span data-stu-id="2955f-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="2955f-112">예제 2: 기존 ExpressRoute 회로에 파이핑을 사용하여 회로 연결 구성 추가</span><span class="sxs-lookup"><span data-stu-id="2955f-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="2955f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2955f-113">PARAMETERS</span></span>

### <span data-ttu-id="2955f-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2955f-114">-AddressPrefix</span></span>
<span data-ttu-id="2955f-115">IPv4 터널에 대한 Express Route 회로 간에 VxLan 터널을 만드는 최소 /29개 고객 주소 공간입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="2955f-116">또는 IPv6 터널에 대한 Express Route 회로 간에 VxLan 터널을 만들 수 있는 최소 /125의 고객 주소 공간입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="2955f-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="2955f-117">-AddressPrefixType</span></span>
<span data-ttu-id="2955f-118">주소가 속한 주소 패밀리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="2955f-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="2955f-119">-AuthorizationKey</span></span>
<span data-ttu-id="2955f-120">다른 구독에서 Express Route 회로를 피어링하는 권한 부여 키입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="2955f-121">기존 명령을 사용하여 피어 회로에 대한 권한 부여를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="2955f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2955f-122">-DefaultProfile</span></span>
<span data-ttu-id="2955f-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2955f-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2955f-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2955f-125">수정되는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="2955f-126">**Get-AzExpressRouteCircuit** cmdlet에서 반환된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="2955f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2955f-127">-Name</span></span>
<span data-ttu-id="2955f-128">추가할 회로 연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="2955f-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="2955f-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="2955f-130">현재 회로와 피어링될 원격 회로의 개인 피어링에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="2955f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2955f-131">-Confirm</span></span>
<span data-ttu-id="2955f-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2955f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2955f-133">-WhatIf</span></span>
<span data-ttu-id="2955f-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2955f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2955f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2955f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2955f-136">CommonParameters</span></span>
<span data-ttu-id="2955f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2955f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2955f-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2955f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2955f-139">입력</span><span class="sxs-lookup"><span data-stu-id="2955f-139">INPUTS</span></span>

### <span data-ttu-id="2955f-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2955f-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="2955f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2955f-141">System.String</span></span>

## <span data-ttu-id="2955f-142">출력</span><span class="sxs-lookup"><span data-stu-id="2955f-142">OUTPUTS</span></span>

### <span data-ttu-id="2955f-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2955f-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2955f-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2955f-144">NOTES</span></span>

## <span data-ttu-id="2955f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2955f-145">RELATED LINKS</span></span>

[<span data-ttu-id="2955f-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2955f-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2955f-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2955f-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2955f-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2955f-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2955f-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2955f-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="2955f-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2955f-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)