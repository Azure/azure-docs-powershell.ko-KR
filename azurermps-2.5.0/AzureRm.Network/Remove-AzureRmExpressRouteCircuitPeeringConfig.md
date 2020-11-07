---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 749f1b84ed033e903d3e50652e6199f184fffa2b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880957"
---
# <span data-ttu-id="4031f-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4031f-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4031f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4031f-102">SYNOPSIS</span></span>
<span data-ttu-id="4031f-103">Express 경로 회로 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4031f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4031f-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4031f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4031f-105">DESCRIPTION</span></span>
<span data-ttu-id="4031f-106">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4031f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4031f-107">EXAMPLES</span></span>

### <span data-ttu-id="4031f-108">예제 1: Express 경로 회로에서 피어 링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="4031f-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="4031f-109">변수</span><span class="sxs-lookup"><span data-stu-id="4031f-109">PARAMETERS</span></span>

### <span data-ttu-id="4031f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4031f-110">-DefaultProfile</span></span>
<span data-ttu-id="4031f-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4031f-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4031f-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4031f-113">제거할 피어 링 구성을 포함 하는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4031f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="4031f-114">-Name</span></span>
<span data-ttu-id="4031f-115">제거할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-115">The name of the peering configuration to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4031f-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4031f-116">-PeerAddressType</span></span>
<span data-ttu-id="4031f-117">피어 링의 주소 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4031f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4031f-118">CommonParameters</span></span>
<span data-ttu-id="4031f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4031f-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4031f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4031f-121">입력</span><span class="sxs-lookup"><span data-stu-id="4031f-121">INPUTS</span></span>

### <span data-ttu-id="4031f-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4031f-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="4031f-123">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4031f-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="4031f-124">출력</span><span class="sxs-lookup"><span data-stu-id="4031f-124">OUTPUTS</span></span>

### <span data-ttu-id="4031f-125">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4031f-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4031f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4031f-126">NOTES</span></span>

## <span data-ttu-id="4031f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4031f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4031f-128">추가-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4031f-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4031f-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4031f-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4031f-130">새로운 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4031f-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4031f-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4031f-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
