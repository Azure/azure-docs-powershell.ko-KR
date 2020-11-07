---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: 0c7beb4bc53635a8bf4293abf50441b0f15b66b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711338"
---
# <span data-ttu-id="5a78a-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="5a78a-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="5a78a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a78a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a78a-103">Express 경로 목록 서비스 공급자 및 해당 특성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a78a-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a78a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a78a-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a78a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a78a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a78a-106">**AzureRmExpressRouteServiceProvider** Cmdlet은 express 경로 기반 서비스 공급자 및 해당 특성 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a78a-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="5a78a-107">특성에는 위치 및 대역폭 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a78a-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="5a78a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5a78a-108">EXAMPLES</span></span>

### <span data-ttu-id="5a78a-109">예제 1: "실리콘 계곡"의 위치를 사용 하 여 서비스 공급자 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="5a78a-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="5a78a-110">변수</span><span class="sxs-lookup"><span data-stu-id="5a78a-110">PARAMETERS</span></span>

### <span data-ttu-id="5a78a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a78a-111">-DefaultProfile</span></span>
<span data-ttu-id="5a78a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a78a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a78a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a78a-113">CommonParameters</span></span>
<span data-ttu-id="5a78a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a78a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a78a-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a78a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a78a-116">입력</span><span class="sxs-lookup"><span data-stu-id="5a78a-116">INPUTS</span></span>

### <span data-ttu-id="5a78a-117">않아야</span><span class="sxs-lookup"><span data-stu-id="5a78a-117">None</span></span>

## <span data-ttu-id="5a78a-118">출력</span><span class="sxs-lookup"><span data-stu-id="5a78a-118">OUTPUTS</span></span>

### <span data-ttu-id="5a78a-119">PSExpressRouteServiceProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5a78a-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="5a78a-120">상속자</span><span class="sxs-lookup"><span data-stu-id="5a78a-120">NOTES</span></span>

## <span data-ttu-id="5a78a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a78a-121">RELATED LINKS</span></span>

[<span data-ttu-id="5a78a-122">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5a78a-122">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5a78a-123">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a78a-123">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="5a78a-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5a78a-124">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="5a78a-125">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="5a78a-125">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
