---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700720"
---
# <span data-ttu-id="176f5-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="176f5-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="176f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176f5-102">SYNOPSIS</span></span>
<span data-ttu-id="176f5-103">회로 연결 구성을 Express 경로 회로의 개인 피어 링에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="176f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="176f5-104">SYNTAX</span></span>

### <span data-ttu-id="176f5-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="176f5-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176f5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="176f5-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176f5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="176f5-107">DESCRIPTION</span></span>
<span data-ttu-id="176f5-108">**AzExpressRouteCircuitConnectionConfig** cmdlet은 대상 경로 회로의 개인 피어 링에 회로 연결 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="176f5-109">이렇게 하면 지역 또는 구독에서 두 개의 Express 경로 회로를 피어 링 할 수 있습니다. **Add-AzExpressRouteCircuitPeeringConfig** 을 실행 한 후에는 Set-AzExpressRouteCircuit cmdlet을 호출 하 여 구성을 활성화 해야 한다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="176f5-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="176f5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="176f5-110">EXAMPLES</span></span>

### <span data-ttu-id="176f5-111">예제 1: 기존 Express 경로에 회로 연결 리소스 추가</span><span class="sxs-lookup"><span data-stu-id="176f5-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="176f5-112">예제 2: 파이프를 사용 하 여 기존 Express 경로 회로에 회로 연결 구성 추가</span><span class="sxs-lookup"><span data-stu-id="176f5-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="176f5-113">변수</span><span class="sxs-lookup"><span data-stu-id="176f5-113">PARAMETERS</span></span>

### <span data-ttu-id="176f5-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="176f5-114">-AddressPrefix</span></span>
<span data-ttu-id="176f5-115">Express 경로 회로 간에 VxLan 터널을 만들기 위한 최소/29 고객 주소 공간</span><span class="sxs-lookup"><span data-stu-id="176f5-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="176f5-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="176f5-116">-AuthorizationKey</span></span>
<span data-ttu-id="176f5-117">다른 구독의 피어 Express 경로 회로에 대 한 인증 키</span><span class="sxs-lookup"><span data-stu-id="176f5-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="176f5-118">피어 회로에 대 한 권한 부여는 기존 명령을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="176f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176f5-119">-DefaultProfile</span></span>
<span data-ttu-id="176f5-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="176f5-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="176f5-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="176f5-122">수정 되는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="176f5-123">**AzExpressRouteCircuit** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="176f5-124">-이름</span><span class="sxs-lookup"><span data-stu-id="176f5-124">-Name</span></span>
<span data-ttu-id="176f5-125">추가할 회로 연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="176f5-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="176f5-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="176f5-127">현재 회로와 peered 되는 원격 회로의 개인 피어 링에 대 한 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="176f5-128">-확인</span><span class="sxs-lookup"><span data-stu-id="176f5-128">-Confirm</span></span>
<span data-ttu-id="176f5-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176f5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176f5-130">-WhatIf</span></span>
<span data-ttu-id="176f5-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="176f5-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176f5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176f5-133">CommonParameters</span></span>
<span data-ttu-id="176f5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="176f5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176f5-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176f5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176f5-136">입력</span><span class="sxs-lookup"><span data-stu-id="176f5-136">INPUTS</span></span>

### <span data-ttu-id="176f5-137">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="176f5-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="176f5-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="176f5-138">System.String</span></span>

## <span data-ttu-id="176f5-139">출력</span><span class="sxs-lookup"><span data-stu-id="176f5-139">OUTPUTS</span></span>

### <span data-ttu-id="176f5-140">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="176f5-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="176f5-141">상속자</span><span class="sxs-lookup"><span data-stu-id="176f5-141">NOTES</span></span>

## <span data-ttu-id="176f5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="176f5-142">RELATED LINKS</span></span>

[<span data-ttu-id="176f5-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="176f5-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="176f5-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="176f5-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="176f5-145">제거-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="176f5-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="176f5-146">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="176f5-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="176f5-147">새로운 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="176f5-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="176f5-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="176f5-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="176f5-149">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="176f5-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)