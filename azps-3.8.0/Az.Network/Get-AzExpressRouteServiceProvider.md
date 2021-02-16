---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 7871625f9313179523fd4fad146107690f68a826
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412523"
---
# <span data-ttu-id="fb5a4-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="fb5a4-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="fb5a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5a4-103">ExpressRoute 서비스 공급자 및 해당 특성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5a4-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="fb5a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb5a4-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb5a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="fb5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="fb5a4-106">**Get-AzExpressRouteServiceProvider** cmdlet은 ExpressRoute 서비스 공급자 및 해당 특성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5a4-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="fb5a4-107">특성에는 위치 및 대역폭 옵션이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb5a4-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="fb5a4-108">예제</span><span class="sxs-lookup"><span data-stu-id="fb5a4-108">EXAMPLES</span></span>

### <span data-ttu-id="fb5a4-109">예제 1: "실리콘밸리"의 위치가 있는 서비스 공급자 목록</span><span class="sxs-lookup"><span data-stu-id="fb5a4-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="fb5a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb5a4-110">PARAMETERS</span></span>

### <span data-ttu-id="fb5a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5a4-111">-DefaultProfile</span></span>
<span data-ttu-id="fb5a4-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb5a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb5a4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5a4-113">CommonParameters</span></span>
<span data-ttu-id="fb5a4-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5a4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb5a4-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb5a4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5a4-116">입력</span><span class="sxs-lookup"><span data-stu-id="fb5a4-116">INPUTS</span></span>

### <span data-ttu-id="fb5a4-117">없음</span><span class="sxs-lookup"><span data-stu-id="fb5a4-117">None</span></span>

## <span data-ttu-id="fb5a4-118">출력</span><span class="sxs-lookup"><span data-stu-id="fb5a4-118">OUTPUTS</span></span>

### <span data-ttu-id="fb5a4-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="fb5a4-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="fb5a4-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb5a4-120">NOTES</span></span>

## <span data-ttu-id="fb5a4-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb5a4-121">RELATED LINKS</span></span>

[<span data-ttu-id="fb5a4-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fb5a4-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="fb5a4-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fb5a4-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="fb5a4-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fb5a4-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="fb5a4-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="fb5a4-125">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
