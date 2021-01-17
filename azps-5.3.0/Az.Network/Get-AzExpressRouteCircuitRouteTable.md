---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 3067df10f3cd1d49b519d6c83defe304fbcf0296
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489940"
---
# <span data-ttu-id="ec80b-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ec80b-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="ec80b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec80b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec80b-103">ExpressRoute 회로에서 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ec80b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec80b-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec80b-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec80b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec80b-106">**Get-AzExpressRouteCircuitRouteTable** cmdlet은 ExpressRoute 회로의 자세한 경로 테이블을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="ec80b-107">경로 테이블은 모든 경로를 표시하거나 특정 피어링 형식에 대한 경로를 표시하도록 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="ec80b-108">경로 테이블을 사용하여 피어링 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="ec80b-109">예제</span><span class="sxs-lookup"><span data-stu-id="ec80b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec80b-110">예제 1: 기본 경로에 대한 경로 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="ec80b-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="ec80b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec80b-111">PARAMETERS</span></span>

### <span data-ttu-id="ec80b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec80b-112">-DefaultProfile</span></span>
<span data-ttu-id="ec80b-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec80b-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ec80b-114">-DevicePath</span></span>
<span data-ttu-id="ec80b-115">이 매개 변수에 허용되는 값은 `Primary``Secondary`</span><span class="sxs-lookup"><span data-stu-id="ec80b-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec80b-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="ec80b-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="ec80b-117">검사할 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec80b-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ec80b-118">-PeeringType</span></span>
<span data-ttu-id="ec80b-119">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ec80b-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec80b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec80b-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec80b-121">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec80b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec80b-122">CommonParameters</span></span>
<span data-ttu-id="ec80b-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec80b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec80b-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec80b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec80b-125">입력</span><span class="sxs-lookup"><span data-stu-id="ec80b-125">INPUTS</span></span>

### <span data-ttu-id="ec80b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ec80b-126">System.String</span></span>

## <span data-ttu-id="ec80b-127">출력</span><span class="sxs-lookup"><span data-stu-id="ec80b-127">OUTPUTS</span></span>

### <span data-ttu-id="ec80b-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="ec80b-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="ec80b-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec80b-129">NOTES</span></span>

## <span data-ttu-id="ec80b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec80b-130">RELATED LINKS</span></span>

[<span data-ttu-id="ec80b-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ec80b-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="ec80b-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ec80b-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ec80b-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="ec80b-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
