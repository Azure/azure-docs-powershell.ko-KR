---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881846"
---
# <span data-ttu-id="fc64b-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fc64b-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="fc64b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc64b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc64b-103">이 (가) Express 회로에서 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc64b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc64b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc64b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc64b-105">DESCRIPTION</span></span>
<span data-ttu-id="fc64b-106">AzureRmExpressRouteCircuitRouteTable cmdlet은이 ( **가)** express 회로의 상세 경로 테이블을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="fc64b-107">경로 테이블에는 모든 경로가 표시 되거나 특정 피어 링 유형에 대 한 경로를 표시 하도록 필터링 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="fc64b-108">경로 테이블을 사용 하 여 피어 링 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="fc64b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc64b-109">EXAMPLES</span></span>

### <span data-ttu-id="fc64b-110">예제 1: 기본 경로의 경로 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="fc64b-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="fc64b-111">변수</span><span class="sxs-lookup"><span data-stu-id="fc64b-111">PARAMETERS</span></span>

### <span data-ttu-id="fc64b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc64b-112">-DefaultProfile</span></span>
<span data-ttu-id="fc64b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc64b-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="fc64b-114">-DevicePath</span></span>
<span data-ttu-id="fc64b-115">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="fc64b-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc64b-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="fc64b-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="fc64b-117">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="fc64b-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="fc64b-118">-PeeringType</span></span>
<span data-ttu-id="fc64b-119">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="fc64b-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="fc64b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc64b-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc64b-121">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="fc64b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc64b-122">CommonParameters</span></span>
<span data-ttu-id="fc64b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc64b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc64b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc64b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc64b-125">입력</span><span class="sxs-lookup"><span data-stu-id="fc64b-125">INPUTS</span></span>

## <span data-ttu-id="fc64b-126">출력</span><span class="sxs-lookup"><span data-stu-id="fc64b-126">OUTPUTS</span></span>

### <span data-ttu-id="fc64b-127">PSExpressRouteCircuitRoutesTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fc64b-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="fc64b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="fc64b-128">NOTES</span></span>

## <span data-ttu-id="fc64b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc64b-129">RELATED LINKS</span></span>

[<span data-ttu-id="fc64b-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fc64b-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="fc64b-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fc64b-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="fc64b-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="fc64b-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
