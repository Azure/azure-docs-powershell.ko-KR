---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214101"
---
# <span data-ttu-id="60f0f-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60f0f-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="60f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="60f0f-103">Express 경로 회로 연결 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="60f0f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60f0f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f0f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="60f0f-106">**AzExpressRouteCircuitConnectionConfig** cmdlet은 지정 된 Express 경로 회로와 연결 된 express 회로 연결 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="60f0f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="60f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="60f0f-108">예제 1: Express 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="60f0f-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="60f0f-109">예제 2: Express 회로에서 파이핑을 사용 하 여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="60f0f-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="60f0f-110">예제 3: 특정 주소 패밀리에 대 한 Express 경로 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="60f0f-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="60f0f-111">예제 4: 특정 주소 패밀리에 대해 Express 경로 회로에서 파이핑을 사용 하 여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="60f0f-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="60f0f-112">변수</span><span class="sxs-lookup"><span data-stu-id="60f0f-112">PARAMETERS</span></span>

### <span data-ttu-id="60f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="60f0f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60f0f-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60f0f-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="60f0f-116">제거할 피어 링 구성을 포함 하는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="60f0f-117">-이름</span><span class="sxs-lookup"><span data-stu-id="60f0f-117">-Name</span></span>
<span data-ttu-id="60f0f-118">제거할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="60f0f-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="60f0f-119">-AddressPrefixType</span></span>
<span data-ttu-id="60f0f-120">구성에서 제거 해야 하는 주소 패밀리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f0f-121">-확인</span><span class="sxs-lookup"><span data-stu-id="60f0f-121">-Confirm</span></span>
<span data-ttu-id="60f0f-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f0f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f0f-123">-WhatIf</span></span>
<span data-ttu-id="60f0f-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60f0f-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f0f-126">CommonParameters</span></span>
<span data-ttu-id="60f0f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60f0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f0f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f0f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f0f-129">입력</span><span class="sxs-lookup"><span data-stu-id="60f0f-129">INPUTS</span></span>

### <span data-ttu-id="60f0f-130">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="60f0f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="60f0f-131">출력</span><span class="sxs-lookup"><span data-stu-id="60f0f-131">OUTPUTS</span></span>

### <span data-ttu-id="60f0f-132">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="60f0f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="60f0f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="60f0f-133">NOTES</span></span>

## <span data-ttu-id="60f0f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60f0f-134">RELATED LINKS</span></span>

[<span data-ttu-id="60f0f-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60f0f-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="60f0f-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60f0f-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60f0f-137">추가-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60f0f-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60f0f-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60f0f-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60f0f-139">새로운 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="60f0f-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="60f0f-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60f0f-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="60f0f-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60f0f-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)