---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bc08305d7aa604dd9c7540573ffb5a199e85b287
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409769"
---
# <span data-ttu-id="b3975-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b3975-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="b3975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3975-102">SYNOPSIS</span></span>
<span data-ttu-id="b3975-103">Express Route 회로의 개인 피어링에 회로 연결 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="b3975-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3975-104">SYNTAX</span></span>

### <span data-ttu-id="b3975-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="b3975-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3975-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3975-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3975-107">설명</span><span class="sxs-lookup"><span data-stu-id="b3975-107">DESCRIPTION</span></span>
<span data-ttu-id="b3975-108">**Add-AzExpressRouteCircuitConnectionConfig** cmdlet은 ExpressRoute 회로에 대한 개인 피어링에 회로 연결 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="b3975-109">이렇게 하면 지역 또는 구독에서 두 Express Route 회로를 피어링할 수 있습니다. **Add-AzExpressRouteCircuitPeeringConfig를** 실행한 후 Set-AzExpressRouteCircuit cmdlet을 호출하여 구성을 활성화해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="b3975-110">예제</span><span class="sxs-lookup"><span data-stu-id="b3975-110">EXAMPLES</span></span>

### <span data-ttu-id="b3975-111">예제 1: 기존 ExpressRoute 회로에 회로 연결 리소스 추가</span><span class="sxs-lookup"><span data-stu-id="b3975-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="b3975-112">예제 2: 기존 ExpressRoute 회로에 파이핑을 사용하여 회로 연결 구성 추가</span><span class="sxs-lookup"><span data-stu-id="b3975-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="b3975-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3975-113">PARAMETERS</span></span>

### <span data-ttu-id="b3975-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b3975-114">-AddressPrefix</span></span>
<span data-ttu-id="b3975-115">Express Route 회로 간에 VxLan 터널을 만드는 최소 /29개 고객 주소 공간</span><span class="sxs-lookup"><span data-stu-id="b3975-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="b3975-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="b3975-116">-AuthorizationKey</span></span>
<span data-ttu-id="b3975-117">다른 구독에서 Express Route 회로를 피어링하는 권한 부여 키입니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="b3975-118">기존 명령을 사용하여 피어 회로에 대한 권한 부여를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="b3975-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3975-119">-DefaultProfile</span></span>
<span data-ttu-id="b3975-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3975-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3975-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b3975-122">수정되는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="b3975-123">**Get-AzExpressRouteCircuit** cmdlet에서 반환된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="b3975-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b3975-124">-Name</span></span>
<span data-ttu-id="b3975-125">추가할 회로 연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="b3975-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="b3975-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="b3975-127">현재 회로와 피어링될 원격 회로의 개인 피어링에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="b3975-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3975-128">-Confirm</span></span>
<span data-ttu-id="b3975-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3975-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3975-130">-WhatIf</span></span>
<span data-ttu-id="b3975-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b3975-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3975-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3975-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3975-133">CommonParameters</span></span>
<span data-ttu-id="b3975-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3975-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3975-135">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3975-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3975-136">입력</span><span class="sxs-lookup"><span data-stu-id="b3975-136">INPUTS</span></span>

### <span data-ttu-id="b3975-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3975-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="b3975-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b3975-138">System.String</span></span>

## <span data-ttu-id="b3975-139">출력</span><span class="sxs-lookup"><span data-stu-id="b3975-139">OUTPUTS</span></span>

### <span data-ttu-id="b3975-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3975-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b3975-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3975-141">NOTES</span></span>

## <span data-ttu-id="b3975-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3975-142">RELATED LINKS</span></span>

[<span data-ttu-id="b3975-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3975-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b3975-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b3975-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b3975-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b3975-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="b3975-146">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3975-146">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="b3975-147">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b3975-147">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
