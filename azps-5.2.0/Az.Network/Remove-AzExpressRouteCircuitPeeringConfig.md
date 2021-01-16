---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366864"
---
# <span data-ttu-id="66a19-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="66a19-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="66a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a19-102">SYNOPSIS</span></span>
<span data-ttu-id="66a19-103">ExpressRoute 회로 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66a19-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="66a19-104">구문</span><span class="sxs-lookup"><span data-stu-id="66a19-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a19-105">설명</span><span class="sxs-lookup"><span data-stu-id="66a19-105">DESCRIPTION</span></span>
<span data-ttu-id="66a19-106">**Remove-AzExpressRouteCircuitPeeringConfig** cmdlet은 ExpressRoute 회로 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66a19-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="66a19-107">예제</span><span class="sxs-lookup"><span data-stu-id="66a19-107">EXAMPLES</span></span>

### <span data-ttu-id="66a19-108">예제 1: ExpressRoute 회로에서 피어링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="66a19-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="66a19-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66a19-109">PARAMETERS</span></span>

### <span data-ttu-id="66a19-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a19-110">-DefaultProfile</span></span>
<span data-ttu-id="66a19-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66a19-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a19-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="66a19-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="66a19-113">제거할 피어링 구성을 포함하는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="66a19-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="66a19-114">-Name</span><span class="sxs-lookup"><span data-stu-id="66a19-114">-Name</span></span>
<span data-ttu-id="66a19-115">제거할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66a19-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="66a19-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="66a19-116">-PeerAddressType</span></span>
<span data-ttu-id="66a19-117">피어링의 주소 패밀리</span><span class="sxs-lookup"><span data-stu-id="66a19-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="66a19-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a19-118">CommonParameters</span></span>
<span data-ttu-id="66a19-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66a19-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a19-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66a19-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a19-121">입력</span><span class="sxs-lookup"><span data-stu-id="66a19-121">INPUTS</span></span>

### <span data-ttu-id="66a19-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="66a19-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="66a19-123">출력</span><span class="sxs-lookup"><span data-stu-id="66a19-123">OUTPUTS</span></span>

### <span data-ttu-id="66a19-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="66a19-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="66a19-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66a19-125">NOTES</span></span>

## <span data-ttu-id="66a19-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66a19-126">RELATED LINKS</span></span>

[<span data-ttu-id="66a19-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="66a19-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="66a19-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="66a19-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="66a19-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="66a19-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="66a19-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="66a19-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
