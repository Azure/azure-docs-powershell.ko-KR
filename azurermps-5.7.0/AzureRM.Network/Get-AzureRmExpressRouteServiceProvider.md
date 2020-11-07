---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: d8d5abedd0deaf5af341995552ad72bef4703058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702150"
---
# <span data-ttu-id="49b7d-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="49b7d-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="49b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="49b7d-103">Express 경로 목록 서비스 공급자 및 해당 특성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49b7d-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49b7d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b7d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="49b7d-106">**AzureRmExpressRouteServiceProvider** Cmdlet은 express 경로 기반 서비스 공급자 및 해당 특성 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b7d-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="49b7d-107">특성에는 위치 및 대역폭 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49b7d-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="49b7d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="49b7d-108">EXAMPLES</span></span>

### <span data-ttu-id="49b7d-109">예제 1: "실리콘 계곡"의 위치를 사용 하 여 서비스 공급자 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="49b7d-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="49b7d-110">변수</span><span class="sxs-lookup"><span data-stu-id="49b7d-110">PARAMETERS</span></span>

### <span data-ttu-id="49b7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b7d-111">-DefaultProfile</span></span>
<span data-ttu-id="49b7d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49b7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b7d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b7d-113">CommonParameters</span></span>
<span data-ttu-id="49b7d-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b7d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b7d-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b7d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b7d-116">입력</span><span class="sxs-lookup"><span data-stu-id="49b7d-116">INPUTS</span></span>

### <span data-ttu-id="49b7d-117">않아야</span><span class="sxs-lookup"><span data-stu-id="49b7d-117">None</span></span>
<span data-ttu-id="49b7d-118">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49b7d-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49b7d-119">출력</span><span class="sxs-lookup"><span data-stu-id="49b7d-119">OUTPUTS</span></span>

### <span data-ttu-id="49b7d-120">PSExpressRouteServiceProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="49b7d-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="49b7d-121">상속자</span><span class="sxs-lookup"><span data-stu-id="49b7d-121">NOTES</span></span>

## <span data-ttu-id="49b7d-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49b7d-122">RELATED LINKS</span></span>

[<span data-ttu-id="49b7d-123">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="49b7d-123">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="49b7d-124">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="49b7d-124">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="49b7d-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="49b7d-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="49b7d-126">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="49b7d-126">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
