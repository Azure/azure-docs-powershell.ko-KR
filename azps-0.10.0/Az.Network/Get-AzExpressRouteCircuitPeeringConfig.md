---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875590"
---
# <span data-ttu-id="cce99-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cce99-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="cce99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce99-102">SYNOPSIS</span></span>
<span data-ttu-id="cce99-103">Express 경로 회로 피어 링 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="cce99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cce99-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cce99-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cce99-105">DESCRIPTION</span></span>
<span data-ttu-id="cce99-106">**AzExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로에 대 한 피어 링 관계의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="cce99-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cce99-107">EXAMPLES</span></span>

### <span data-ttu-id="cce99-108">예제 1: Express 경로 회로에 대 한 피어 링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="cce99-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="cce99-109">변수</span><span class="sxs-lookup"><span data-stu-id="cce99-109">PARAMETERS</span></span>

### <span data-ttu-id="cce99-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce99-110">-DefaultProfile</span></span>
<span data-ttu-id="cce99-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce99-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cce99-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cce99-113">피어 링 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="cce99-114">-이름</span><span class="sxs-lookup"><span data-stu-id="cce99-114">-Name</span></span>
<span data-ttu-id="cce99-115">검색할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="cce99-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce99-116">CommonParameters</span></span>
<span data-ttu-id="cce99-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce99-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce99-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce99-119">입력</span><span class="sxs-lookup"><span data-stu-id="cce99-119">INPUTS</span></span>

### <span data-ttu-id="cce99-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cce99-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="cce99-121">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cce99-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="cce99-122">출력</span><span class="sxs-lookup"><span data-stu-id="cce99-122">OUTPUTS</span></span>

### <span data-ttu-id="cce99-123">PSPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cce99-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="cce99-124">상속자</span><span class="sxs-lookup"><span data-stu-id="cce99-124">NOTES</span></span>

## <span data-ttu-id="cce99-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cce99-125">RELATED LINKS</span></span>

[<span data-ttu-id="cce99-126">추가-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cce99-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cce99-127">새로운 AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cce99-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cce99-128">제거-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cce99-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cce99-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cce99-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
