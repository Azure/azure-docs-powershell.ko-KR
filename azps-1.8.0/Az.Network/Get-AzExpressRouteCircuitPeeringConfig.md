---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700599"
---
# <span data-ttu-id="cde7a-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cde7a-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="cde7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde7a-102">SYNOPSIS</span></span>
<span data-ttu-id="cde7a-103">Express 경로 회로 피어 링 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cde7a-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="cde7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cde7a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cde7a-105">DESCRIPTION</span></span>
<span data-ttu-id="cde7a-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로에 대 한 피어 링 관계의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cde7a-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="cde7a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cde7a-107">EXAMPLES</span></span>

### <span data-ttu-id="cde7a-108">예제 1: Express 경로 회로에 대 한 피어 링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="cde7a-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="cde7a-109">변수</span><span class="sxs-lookup"><span data-stu-id="cde7a-109">PARAMETERS</span></span>

### <span data-ttu-id="cde7a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde7a-110">-DefaultProfile</span></span>
<span data-ttu-id="cde7a-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cde7a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde7a-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cde7a-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cde7a-113">피어 링 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cde7a-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="cde7a-114">-이름</span><span class="sxs-lookup"><span data-stu-id="cde7a-114">-Name</span></span>
<span data-ttu-id="cde7a-115">검색할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cde7a-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="cde7a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde7a-116">CommonParameters</span></span>
<span data-ttu-id="cde7a-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cde7a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde7a-118">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cde7a-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde7a-119">입력</span><span class="sxs-lookup"><span data-stu-id="cde7a-119">INPUTS</span></span>

### <span data-ttu-id="cde7a-120">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cde7a-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cde7a-121">출력</span><span class="sxs-lookup"><span data-stu-id="cde7a-121">OUTPUTS</span></span>

### <span data-ttu-id="cde7a-122">PSPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cde7a-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="cde7a-123">상속자</span><span class="sxs-lookup"><span data-stu-id="cde7a-123">NOTES</span></span>

## <span data-ttu-id="cde7a-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cde7a-124">RELATED LINKS</span></span>

[<span data-ttu-id="cde7a-125">추가-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cde7a-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cde7a-126">새로운 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cde7a-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cde7a-127">제거-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cde7a-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cde7a-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cde7a-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
