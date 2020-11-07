---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 223f2a02dcf6d2310109b41587126f374a6733b1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93711920"
---
# <span data-ttu-id="ed9bd-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ed9bd-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ed9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9bd-103">Express 경로 회로 피어 링 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed9bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed9bd-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed9bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed9bd-105">DESCRIPTION</span></span>
<span data-ttu-id="ed9bd-106">**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로에 대 한 피어 링 관계의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ed9bd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ed9bd-107">EXAMPLES</span></span>

### <span data-ttu-id="ed9bd-108">예제 1: Express 경로 회로에 대 한 피어 링 구성 표시</span><span class="sxs-lookup"><span data-stu-id="ed9bd-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="ed9bd-109">변수</span><span class="sxs-lookup"><span data-stu-id="ed9bd-109">PARAMETERS</span></span>

### <span data-ttu-id="ed9bd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9bd-110">-DefaultProfile</span></span>
<span data-ttu-id="ed9bd-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed9bd-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed9bd-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ed9bd-113">피어 링 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="ed9bd-114">-이름</span><span class="sxs-lookup"><span data-stu-id="ed9bd-114">-Name</span></span>
<span data-ttu-id="ed9bd-115">검색할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="ed9bd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9bd-116">CommonParameters</span></span>
<span data-ttu-id="ed9bd-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9bd-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed9bd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9bd-119">입력</span><span class="sxs-lookup"><span data-stu-id="ed9bd-119">INPUTS</span></span>

### <span data-ttu-id="ed9bd-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed9bd-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ed9bd-121">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="ed9bd-122">출력</span><span class="sxs-lookup"><span data-stu-id="ed9bd-122">OUTPUTS</span></span>

### <span data-ttu-id="ed9bd-123">PSPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ed9bd-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="ed9bd-124">상속자</span><span class="sxs-lookup"><span data-stu-id="ed9bd-124">NOTES</span></span>

## <span data-ttu-id="ed9bd-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed9bd-125">RELATED LINKS</span></span>

[<span data-ttu-id="ed9bd-126">추가-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ed9bd-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ed9bd-127">새로운 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ed9bd-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ed9bd-128">제거-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ed9bd-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ed9bd-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ed9bd-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
