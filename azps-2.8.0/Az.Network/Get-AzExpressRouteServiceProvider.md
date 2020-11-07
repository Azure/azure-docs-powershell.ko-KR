---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870697"
---
# <span data-ttu-id="eedca-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="eedca-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="eedca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eedca-102">SYNOPSIS</span></span>
<span data-ttu-id="eedca-103">Express 경로 목록 서비스 공급자 및 해당 특성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="eedca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eedca-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eedca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eedca-105">DESCRIPTION</span></span>
<span data-ttu-id="eedca-106">**AzExpressRouteServiceProvider** Cmdlet은 express 경로 기반 서비스 공급자 및 해당 특성 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="eedca-107">특성에는 위치 및 대역폭 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="eedca-108">예제의</span><span class="sxs-lookup"><span data-stu-id="eedca-108">EXAMPLES</span></span>

### <span data-ttu-id="eedca-109">예제 1: "실리콘 계곡"의 위치를 사용 하 여 서비스 공급자 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="eedca-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="eedca-110">변수</span><span class="sxs-lookup"><span data-stu-id="eedca-110">PARAMETERS</span></span>

### <span data-ttu-id="eedca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eedca-111">-DefaultProfile</span></span>
<span data-ttu-id="eedca-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eedca-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eedca-113">CommonParameters</span></span>
<span data-ttu-id="eedca-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eedca-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eedca-115">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eedca-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eedca-116">입력</span><span class="sxs-lookup"><span data-stu-id="eedca-116">INPUTS</span></span>

### <span data-ttu-id="eedca-117">않아야</span><span class="sxs-lookup"><span data-stu-id="eedca-117">None</span></span>

## <span data-ttu-id="eedca-118">출력</span><span class="sxs-lookup"><span data-stu-id="eedca-118">OUTPUTS</span></span>

### <span data-ttu-id="eedca-119">PSExpressRouteServiceProvider에 대 한.</span><span class="sxs-lookup"><span data-stu-id="eedca-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="eedca-120">상속자</span><span class="sxs-lookup"><span data-stu-id="eedca-120">NOTES</span></span>

## <span data-ttu-id="eedca-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eedca-121">RELATED LINKS</span></span>

[<span data-ttu-id="eedca-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="eedca-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="eedca-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eedca-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="eedca-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eedca-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="eedca-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="eedca-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
