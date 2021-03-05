---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996403"
---
# <span data-ttu-id="5a46c-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a46c-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="5a46c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a46c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a46c-103">ExpressRoute 회로 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5a46c-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="5a46c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a46c-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a46c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5a46c-105">DESCRIPTION</span></span>
<span data-ttu-id="5a46c-106">**Remove-AzExpressRouteCircuitPeeringConfig** cmdlet은 ExpressRoute 회로 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5a46c-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="5a46c-107">예제</span><span class="sxs-lookup"><span data-stu-id="5a46c-107">EXAMPLES</span></span>

### <span data-ttu-id="5a46c-108">예제 1: ExpressRoute 회로에서 피어링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5a46c-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="5a46c-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5a46c-109">PARAMETERS</span></span>

### <span data-ttu-id="5a46c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a46c-110">-DefaultProfile</span></span>
<span data-ttu-id="5a46c-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a46c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a46c-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a46c-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5a46c-113">제거할 피어링 구성을 포함하는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="5a46c-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5a46c-114">-Name</span></span>
<span data-ttu-id="5a46c-115">제거할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a46c-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="5a46c-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="5a46c-116">-PeerAddressType</span></span>
<span data-ttu-id="5a46c-117">피어링의 주소 패밀리</span><span class="sxs-lookup"><span data-stu-id="5a46c-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a46c-118">CommonParameters</span></span>
<span data-ttu-id="5a46c-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a46c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a46c-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5a46c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a46c-121">입력</span><span class="sxs-lookup"><span data-stu-id="5a46c-121">INPUTS</span></span>

### <span data-ttu-id="5a46c-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a46c-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5a46c-123">출력</span><span class="sxs-lookup"><span data-stu-id="5a46c-123">OUTPUTS</span></span>

### <span data-ttu-id="5a46c-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a46c-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5a46c-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a46c-125">NOTES</span></span>

## <span data-ttu-id="5a46c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a46c-126">RELATED LINKS</span></span>

[<span data-ttu-id="5a46c-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a46c-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5a46c-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a46c-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5a46c-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5a46c-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5a46c-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a46c-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
