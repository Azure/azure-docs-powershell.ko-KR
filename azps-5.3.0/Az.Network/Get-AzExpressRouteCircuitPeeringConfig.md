---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489948"
---
# <span data-ttu-id="70f33-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="70f33-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="70f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f33-102">SYNOPSIS</span></span>
<span data-ttu-id="70f33-103">ExpressRoute 회로 피어링 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="70f33-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="70f33-104">구문</span><span class="sxs-lookup"><span data-stu-id="70f33-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70f33-105">설명</span><span class="sxs-lookup"><span data-stu-id="70f33-105">DESCRIPTION</span></span>
<span data-ttu-id="70f33-106">**Get-AzExpressRouteCircuitPeeringConfig** cmdlet은 ExpressRoute 회로에 대한 피어링 관계의 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="70f33-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="70f33-107">예제</span><span class="sxs-lookup"><span data-stu-id="70f33-107">EXAMPLES</span></span>

### <span data-ttu-id="70f33-108">예제 1: ExpressRoute 회로에 대한 피어링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="70f33-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="70f33-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70f33-109">PARAMETERS</span></span>

### <span data-ttu-id="70f33-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f33-110">-DefaultProfile</span></span>
<span data-ttu-id="70f33-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70f33-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f33-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70f33-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="70f33-113">피어링 구성을 포함하는 ExpressRoute 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="70f33-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="70f33-114">-Name</span><span class="sxs-lookup"><span data-stu-id="70f33-114">-Name</span></span>
<span data-ttu-id="70f33-115">검색할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70f33-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="70f33-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f33-116">CommonParameters</span></span>
<span data-ttu-id="70f33-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70f33-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f33-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70f33-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f33-119">입력</span><span class="sxs-lookup"><span data-stu-id="70f33-119">INPUTS</span></span>

### <span data-ttu-id="70f33-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70f33-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="70f33-121">출력</span><span class="sxs-lookup"><span data-stu-id="70f33-121">OUTPUTS</span></span>

### <span data-ttu-id="70f33-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="70f33-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="70f33-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70f33-123">NOTES</span></span>

## <span data-ttu-id="70f33-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70f33-124">RELATED LINKS</span></span>

[<span data-ttu-id="70f33-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="70f33-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="70f33-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="70f33-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="70f33-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="70f33-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="70f33-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="70f33-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
