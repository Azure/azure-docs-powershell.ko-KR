---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535804"
---
# <span data-ttu-id="d2bc0-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d2bc0-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="d2bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2bc0-103">회로 연결 구성을 Express 경로 회로의 개인 피어 링에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2bc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2bc0-104">SYNTAX</span></span>

### <span data-ttu-id="d2bc0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2bc0-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2bc0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2bc0-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2bc0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="d2bc0-108">**AzureRmExpressRouteCircuitConnectionConfig** cmdlet은 대상 경로 회로의 개인 피어 링에 회로 연결 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="d2bc0-109">이렇게 하면 지역 또는 구독에서 두 개의 Express 경로 회로를 피어 링 할 수 있습니다. **Add-AzureRmExpressRouteCircuitPeeringConfig** 을 실행 한 후에는 Set-AzureRmExpressRouteCircuit cmdlet을 호출 하 여 구성을 활성화 해야 한다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="d2bc0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d2bc0-110">EXAMPLES</span></span>

### <span data-ttu-id="d2bc0-111">예제 1: 기존 Express 경로에 회로 연결 리소스 추가</span><span class="sxs-lookup"><span data-stu-id="d2bc0-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="d2bc0-112">예제 2: 파이프를 사용 하 여 기존 Express 경로 회로에 회로 연결 구성 추가</span><span class="sxs-lookup"><span data-stu-id="d2bc0-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="d2bc0-113">변수</span><span class="sxs-lookup"><span data-stu-id="d2bc0-113">PARAMETERS</span></span>

### <span data-ttu-id="d2bc0-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d2bc0-114">-AddressPrefix</span></span>
<span data-ttu-id="d2bc0-115">Express 경로 회로 간에 VxLan 터널을 만들기 위한 최소/29 고객 주소 공간</span><span class="sxs-lookup"><span data-stu-id="d2bc0-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="d2bc0-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="d2bc0-116">-AuthorizationKey</span></span>
<span data-ttu-id="d2bc0-117">다른 구독의 피어 Express 경로 회로에 대 한 인증 키</span><span class="sxs-lookup"><span data-stu-id="d2bc0-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="d2bc0-118">피어 회로에 대 한 권한 부여는 기존 명령을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="d2bc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2bc0-119">-DefaultProfile</span></span>
<span data-ttu-id="d2bc0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2bc0-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d2bc0-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d2bc0-122">수정 되는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="d2bc0-123">**AzureRmExpressRouteCircuit** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="d2bc0-124">-이름</span><span class="sxs-lookup"><span data-stu-id="d2bc0-124">-Name</span></span>
<span data-ttu-id="d2bc0-125">추가할 회로 연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="d2bc0-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="d2bc0-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="d2bc0-127">현재 회로와 peered 되는 원격 회로의 개인 피어 링에 대 한 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="d2bc0-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d2bc0-128">-Confirm</span></span>
<span data-ttu-id="d2bc0-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2bc0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2bc0-130">-WhatIf</span></span>
<span data-ttu-id="d2bc0-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2bc0-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2bc0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2bc0-133">CommonParameters</span></span>
<span data-ttu-id="d2bc0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2bc0-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2bc0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2bc0-136">입력</span><span class="sxs-lookup"><span data-stu-id="d2bc0-136">INPUTS</span></span>

### <span data-ttu-id="d2bc0-137">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="d2bc0-138">매개 변수: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2bc0-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="d2bc0-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2bc0-139">System.String</span></span>

## <span data-ttu-id="d2bc0-140">출력</span><span class="sxs-lookup"><span data-stu-id="d2bc0-140">OUTPUTS</span></span>

### <span data-ttu-id="d2bc0-141">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d2bc0-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d2bc0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d2bc0-142">NOTES</span></span>

## <span data-ttu-id="d2bc0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2bc0-143">RELATED LINKS</span></span>

[<span data-ttu-id="d2bc0-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d2bc0-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d2bc0-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d2bc0-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d2bc0-146">제거-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d2bc0-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d2bc0-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d2bc0-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d2bc0-148">새로운 AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d2bc0-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d2bc0-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d2bc0-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d2bc0-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d2bc0-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
