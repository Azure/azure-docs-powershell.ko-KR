---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
ms.openlocfilehash: 68579ea2adecbf7ad6a97fd11f4f32da9adeb48f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882641"
---
# <span data-ttu-id="737f0-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="737f0-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="737f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737f0-102">SYNOPSIS</span></span>
<span data-ttu-id="737f0-103">Express 경로 회로의 사용 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="737f0-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="737f0-105">DESCRIPTION</span></span>
<span data-ttu-id="737f0-106">**AzureRmExpressRouteCircuitStats** Cmdlet은 express 경로 회로에 대 한 트래픽 통계를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="737f0-107">통계에는 기본 및 보조 경로를 통해 주고 받은 바이트 수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="737f0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="737f0-108">EXAMPLES</span></span>

### <span data-ttu-id="737f0-109">예제 1: Express 경로 피어에 대 한 트래픽 통계 표시</span><span class="sxs-lookup"><span data-stu-id="737f0-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="737f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="737f0-110">PARAMETERS</span></span>

### <span data-ttu-id="737f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737f0-111">-DefaultProfile</span></span>
<span data-ttu-id="737f0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="737f0-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="737f0-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="737f0-114">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737f0-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="737f0-115">-PeeringType</span></span>
<span data-ttu-id="737f0-116">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="737f0-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="737f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="737f0-118">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737f0-119">CommonParameters</span></span>
<span data-ttu-id="737f0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="737f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737f0-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737f0-122">입력</span><span class="sxs-lookup"><span data-stu-id="737f0-122">INPUTS</span></span>

## <span data-ttu-id="737f0-123">출력</span><span class="sxs-lookup"><span data-stu-id="737f0-123">OUTPUTS</span></span>

### <span data-ttu-id="737f0-124">PSExpressRouteCircuitStats에 대 한.</span><span class="sxs-lookup"><span data-stu-id="737f0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="737f0-125">상속자</span><span class="sxs-lookup"><span data-stu-id="737f0-125">NOTES</span></span>

## <span data-ttu-id="737f0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="737f0-126">RELATED LINKS</span></span>

[<span data-ttu-id="737f0-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="737f0-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="737f0-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="737f0-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="737f0-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="737f0-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
