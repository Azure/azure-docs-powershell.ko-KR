---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875341"
---
# <span data-ttu-id="ee45d-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ee45d-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ee45d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee45d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee45d-103">Express 경로 회로 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ee45d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee45d-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee45d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee45d-105">DESCRIPTION</span></span>
<span data-ttu-id="ee45d-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ee45d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee45d-107">EXAMPLES</span></span>

### <span data-ttu-id="ee45d-108">예제 1: Express 경로 회로에서 피어 링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="ee45d-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="ee45d-109">변수</span><span class="sxs-lookup"><span data-stu-id="ee45d-109">PARAMETERS</span></span>

### <span data-ttu-id="ee45d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee45d-110">-DefaultProfile</span></span>
<span data-ttu-id="ee45d-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee45d-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee45d-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ee45d-113">제거할 피어 링 구성을 포함 하는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ee45d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="ee45d-114">-Name</span></span>
<span data-ttu-id="ee45d-115">제거할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ee45d-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ee45d-116">-PeerAddressType</span></span>
<span data-ttu-id="ee45d-117">피어 링의 주소 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="ee45d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee45d-118">CommonParameters</span></span>
<span data-ttu-id="ee45d-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee45d-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee45d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee45d-121">입력</span><span class="sxs-lookup"><span data-stu-id="ee45d-121">INPUTS</span></span>

### <span data-ttu-id="ee45d-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee45d-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ee45d-123">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee45d-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="ee45d-124">출력</span><span class="sxs-lookup"><span data-stu-id="ee45d-124">OUTPUTS</span></span>

### <span data-ttu-id="ee45d-125">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ee45d-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ee45d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ee45d-126">NOTES</span></span>

## <span data-ttu-id="ee45d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee45d-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee45d-128">추가-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ee45d-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ee45d-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee45d-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ee45d-130">새로운 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ee45d-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ee45d-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ee45d-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
