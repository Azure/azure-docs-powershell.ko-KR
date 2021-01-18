---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493183"
---
# <span data-ttu-id="6c589-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c589-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="6c589-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c589-102">SYNOPSIS</span></span>
<span data-ttu-id="6c589-103">ExpressRoute 회로 연결 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="6c589-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c589-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c589-105">설명</span><span class="sxs-lookup"><span data-stu-id="6c589-105">DESCRIPTION</span></span>
<span data-ttu-id="6c589-106">**Remove-AzExpressRouteCircuitConnectionConfig** cmdlet은 주어진 ExpressRoute 회로와 연결된 ExpressRoute 회로 연결 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="6c589-107">예제</span><span class="sxs-lookup"><span data-stu-id="6c589-107">EXAMPLES</span></span>

### <span data-ttu-id="6c589-108">예제 1: ExpressRoute 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="6c589-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="6c589-109">예제 2: ExpressRoute 회로에서 Piping을 사용하여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="6c589-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="6c589-110">예제 3: 특정 주소 패밀리에 대한 ExpressRoute 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="6c589-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="6c589-111">예제 4: 특정 주소 패밀리에 대한 ExpressRoute 회로에서 Piping을 사용하여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="6c589-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="6c589-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c589-112">PARAMETERS</span></span>

### <span data-ttu-id="6c589-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c589-113">-DefaultProfile</span></span>
<span data-ttu-id="6c589-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c589-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6c589-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6c589-116">제거할 피어링 구성을 포함하는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="6c589-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6c589-117">-Name</span></span>
<span data-ttu-id="6c589-118">제거할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="6c589-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="6c589-119">-AddressPrefixType</span></span>
<span data-ttu-id="6c589-120">구성에서 제거해야 하는 주소 패밀리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="6c589-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c589-121">-Confirm</span></span>
<span data-ttu-id="6c589-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c589-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c589-123">-WhatIf</span></span>
<span data-ttu-id="6c589-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6c589-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c589-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c589-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c589-126">CommonParameters</span></span>
<span data-ttu-id="6c589-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c589-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c589-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6c589-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c589-129">입력</span><span class="sxs-lookup"><span data-stu-id="6c589-129">INPUTS</span></span>

### <span data-ttu-id="6c589-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6c589-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6c589-131">출력</span><span class="sxs-lookup"><span data-stu-id="6c589-131">OUTPUTS</span></span>

### <span data-ttu-id="6c589-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6c589-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6c589-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c589-133">NOTES</span></span>

## <span data-ttu-id="6c589-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c589-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c589-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6c589-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="6c589-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c589-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6c589-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c589-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6c589-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c589-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6c589-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6c589-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="6c589-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6c589-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="6c589-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6c589-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)