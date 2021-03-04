---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7da632a1496b22e2f0be183640995a2aaa96735e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007787"
---
# <span data-ttu-id="a9d01-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9d01-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a9d01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d01-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d01-103">ExpressRoute 회로 피어링 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9d01-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a9d01-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9d01-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d01-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9d01-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d01-106">**Get-AzExpressRouteCircuitPeeringConfig** cmdlet은 ExpressRoute 회로에 대한 피어링 관계의 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d01-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="a9d01-107">예제</span><span class="sxs-lookup"><span data-stu-id="a9d01-107">EXAMPLES</span></span>

### <span data-ttu-id="a9d01-108">예제 1: ExpressRoute 회로에 대한 피어링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="a9d01-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="a9d01-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9d01-109">PARAMETERS</span></span>

### <span data-ttu-id="a9d01-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d01-110">-DefaultProfile</span></span>
<span data-ttu-id="a9d01-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9d01-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d01-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d01-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a9d01-113">피어링 구성을 포함하는 ExpressRoute 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a9d01-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="a9d01-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a9d01-114">-Name</span></span>
<span data-ttu-id="a9d01-115">검색할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9d01-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="a9d01-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d01-116">CommonParameters</span></span>
<span data-ttu-id="a9d01-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9d01-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d01-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9d01-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d01-119">입력</span><span class="sxs-lookup"><span data-stu-id="a9d01-119">INPUTS</span></span>

### <span data-ttu-id="a9d01-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d01-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a9d01-121">출력</span><span class="sxs-lookup"><span data-stu-id="a9d01-121">OUTPUTS</span></span>

### <span data-ttu-id="a9d01-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="a9d01-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="a9d01-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9d01-123">NOTES</span></span>

## <span data-ttu-id="a9d01-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9d01-124">RELATED LINKS</span></span>

[<span data-ttu-id="a9d01-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9d01-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a9d01-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9d01-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a9d01-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a9d01-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a9d01-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a9d01-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
