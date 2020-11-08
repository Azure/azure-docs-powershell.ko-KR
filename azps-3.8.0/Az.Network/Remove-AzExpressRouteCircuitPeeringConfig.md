---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044067"
---
# <span data-ttu-id="c6d09-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c6d09-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c6d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d09-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d09-103">Express 경로 회로 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="c6d09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6d09-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6d09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6d09-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d09-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="c6d09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6d09-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d09-108">예제 1: Express 경로 회로에서 피어 링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="c6d09-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="c6d09-109">변수</span><span class="sxs-lookup"><span data-stu-id="c6d09-109">PARAMETERS</span></span>

### <span data-ttu-id="c6d09-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d09-110">-DefaultProfile</span></span>
<span data-ttu-id="c6d09-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6d09-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6d09-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c6d09-113">제거할 피어 링 구성을 포함 하는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c6d09-114">-이름</span><span class="sxs-lookup"><span data-stu-id="c6d09-114">-Name</span></span>
<span data-ttu-id="c6d09-115">제거할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c6d09-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c6d09-116">-PeerAddressType</span></span>
<span data-ttu-id="c6d09-117">피어 링의 주소 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="c6d09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d09-118">CommonParameters</span></span>
<span data-ttu-id="c6d09-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d09-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d09-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d09-121">입력</span><span class="sxs-lookup"><span data-stu-id="c6d09-121">INPUTS</span></span>

### <span data-ttu-id="c6d09-122">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c6d09-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c6d09-123">출력</span><span class="sxs-lookup"><span data-stu-id="c6d09-123">OUTPUTS</span></span>

### <span data-ttu-id="c6d09-124">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c6d09-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c6d09-125">상속자</span><span class="sxs-lookup"><span data-stu-id="c6d09-125">NOTES</span></span>

## <span data-ttu-id="c6d09-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6d09-126">RELATED LINKS</span></span>

[<span data-ttu-id="c6d09-127">추가-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c6d09-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c6d09-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6d09-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="c6d09-129">새로운 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c6d09-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c6d09-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6d09-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
