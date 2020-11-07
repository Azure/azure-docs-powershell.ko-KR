---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 4577eb4f105bca235e7b5e9feb0b0ef308298881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702259"
---
# <span data-ttu-id="0ae16-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="0ae16-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="0ae16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae16-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae16-103">Express 경로 회로의 사용 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ae16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ae16-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ae16-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ae16-105">DESCRIPTION</span></span>
<span data-ttu-id="0ae16-106">**AzureRmExpressRouteCircuitStats** Cmdlet은 express 경로 회로에 대 한 트래픽 통계를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="0ae16-107">통계에는 기본 및 보조 경로를 통해 주고 받은 바이트 수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="0ae16-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0ae16-108">EXAMPLES</span></span>

### <span data-ttu-id="0ae16-109">예제 1: Express 경로 피어에 대 한 트래픽 통계 표시</span><span class="sxs-lookup"><span data-stu-id="0ae16-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="0ae16-110">변수</span><span class="sxs-lookup"><span data-stu-id="0ae16-110">PARAMETERS</span></span>

### <span data-ttu-id="0ae16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae16-111">-DefaultProfile</span></span>
<span data-ttu-id="0ae16-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ae16-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="0ae16-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="0ae16-114">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="0ae16-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0ae16-115">-PeeringType</span></span>
<span data-ttu-id="0ae16-116">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0ae16-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0ae16-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ae16-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ae16-118">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="0ae16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae16-119">CommonParameters</span></span>
<span data-ttu-id="0ae16-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae16-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ae16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae16-122">입력</span><span class="sxs-lookup"><span data-stu-id="0ae16-122">INPUTS</span></span>

### <span data-ttu-id="0ae16-123">않아야</span><span class="sxs-lookup"><span data-stu-id="0ae16-123">None</span></span>
<span data-ttu-id="0ae16-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ae16-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ae16-125">출력</span><span class="sxs-lookup"><span data-stu-id="0ae16-125">OUTPUTS</span></span>

### <span data-ttu-id="0ae16-126">PSExpressRouteCircuitStats에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0ae16-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="0ae16-127">상속자</span><span class="sxs-lookup"><span data-stu-id="0ae16-127">NOTES</span></span>

## <span data-ttu-id="0ae16-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae16-128">RELATED LINKS</span></span>

[<span data-ttu-id="0ae16-129">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0ae16-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="0ae16-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0ae16-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="0ae16-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0ae16-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
