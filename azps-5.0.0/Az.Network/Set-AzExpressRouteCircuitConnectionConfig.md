---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310151"
---
# <span data-ttu-id="7b392-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b392-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="7b392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b392-102">SYNOPSIS</span></span>
<span data-ttu-id="7b392-103">Express 경로 회로에 대해 전용 Peerings에서 생성 된 회로 연결 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="7b392-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b392-104">SYNTAX</span></span>

### <span data-ttu-id="7b392-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b392-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b392-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b392-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b392-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7b392-107">DESCRIPTION</span></span>
<span data-ttu-id="7b392-108">**AzExpressRouteCircuitConnectionConfig** Cmdlet은 express 경로 회로의 개인 피어 링에서 생성 된 회로 연결 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="7b392-109">이렇게 하면 지역 또는 구독에서 두 개의 Express 경로 회로를 피어 링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="7b392-110">**AzExpressRouteCircuitConnectionConfig** 를 실행 하기 전에 **add-AzExpressRouteCircuitConnectionConfig** 를 사용 하 여 회로 연결을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="7b392-111">또한 **Set-AzExpressRouteCircuitPeeringConfig** 을 실행 한 후에는 Set-AzExpressRouteCircuit cmdlet을 호출 하 여 구성을 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="7b392-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7b392-112">EXAMPLES</span></span>

### <span data-ttu-id="7b392-113">예제 1: 기존 Express 회로에 대 한 회로 연결 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="7b392-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="7b392-114">예제 2: 파이프를 사용 하 여 기존 Express 경로 회로에 대 한 회로 연결 구성 설정</span><span class="sxs-lookup"><span data-stu-id="7b392-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="7b392-115">변수</span><span class="sxs-lookup"><span data-stu-id="7b392-115">PARAMETERS</span></span>

### <span data-ttu-id="7b392-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7b392-116">-AddressPrefix</span></span>
<span data-ttu-id="7b392-117">IPv4 터널에 대 한 Express 경로 회로 간에 VxLan 터널을 만들기 위한 최소/29 고객 주소 공간.</span><span class="sxs-lookup"><span data-stu-id="7b392-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="7b392-118">또는 IPv6 터널에 대 한 Express 경로 회로 간에 VxLan 터널을 만들기 위한 최소/125 고객 주소 공간.</span><span class="sxs-lookup"><span data-stu-id="7b392-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="7b392-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="7b392-119">-AddressPrefixType</span></span>
<span data-ttu-id="7b392-120">주소 접두사가 속한 주소 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="7b392-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7b392-121">-AuthorizationKey</span></span>
<span data-ttu-id="7b392-122">다른 구독의 피어 Express 경로 회로에 대 한 인증 키</span><span class="sxs-lookup"><span data-stu-id="7b392-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="7b392-123">피어 회로에 대 한 권한 부여는 기존 명령을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="7b392-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b392-124">-DefaultProfile</span></span>
<span data-ttu-id="7b392-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b392-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b392-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7b392-127">수정 되는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="7b392-128">**AzExpressRouteCircuit** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="7b392-129">-이름</span><span class="sxs-lookup"><span data-stu-id="7b392-129">-Name</span></span>
<span data-ttu-id="7b392-130">추가할 회로 연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="7b392-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="7b392-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="7b392-132">현재 회로와 peered 되는 원격 회로의 개인 피어 링에 대 한 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="7b392-133">-확인</span><span class="sxs-lookup"><span data-stu-id="7b392-133">-Confirm</span></span>
<span data-ttu-id="7b392-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b392-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b392-135">-WhatIf</span></span>
<span data-ttu-id="7b392-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b392-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b392-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b392-138">CommonParameters</span></span>
<span data-ttu-id="7b392-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b392-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b392-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b392-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b392-141">입력</span><span class="sxs-lookup"><span data-stu-id="7b392-141">INPUTS</span></span>

### <span data-ttu-id="7b392-142">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7b392-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="7b392-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b392-143">System.String</span></span>

## <span data-ttu-id="7b392-144">출력</span><span class="sxs-lookup"><span data-stu-id="7b392-144">OUTPUTS</span></span>

### <span data-ttu-id="7b392-145">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7b392-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7b392-146">상속자</span><span class="sxs-lookup"><span data-stu-id="7b392-146">NOTES</span></span>

## <span data-ttu-id="7b392-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b392-147">RELATED LINKS</span></span>

[<span data-ttu-id="7b392-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b392-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b392-149">제거-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b392-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b392-150">추가-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="7b392-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="7b392-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b392-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="7b392-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b392-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
