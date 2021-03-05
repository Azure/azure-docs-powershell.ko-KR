---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 14277d7e3bdd8f1930cd627ac936a4e5d6d8e2f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006464"
---
# <span data-ttu-id="e7504-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e7504-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="e7504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7504-102">SYNOPSIS</span></span>
<span data-ttu-id="e7504-103">ExpressRoute 회로의 경로 테이블 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e7504-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7504-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7504-105">설명</span><span class="sxs-lookup"><span data-stu-id="e7504-105">DESCRIPTION</span></span>
<span data-ttu-id="e7504-106">**Get-AzExpressRouteCircuitRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대한 BGP 인접 정보 요약을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="e7504-107">이 정보는 라우팅 컨텍스트가 설정된 기간 및 피어링 라우터에서 보급하는 경로의 수를 결정하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="e7504-108">예제</span><span class="sxs-lookup"><span data-stu-id="e7504-108">EXAMPLES</span></span>

### <span data-ttu-id="e7504-109">예제 1: 기본 경로에 대한 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="e7504-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="e7504-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7504-110">PARAMETERS</span></span>

### <span data-ttu-id="e7504-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7504-111">-DefaultProfile</span></span>
<span data-ttu-id="e7504-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7504-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="e7504-113">-DevicePath</span></span>
<span data-ttu-id="e7504-114">이 매개 변수에 대해 허용되는 값은 다음 `Primary` 또는 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="e7504-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="e7504-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="e7504-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="e7504-116">검사되는 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="e7504-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e7504-117">-PeeringType</span></span>
<span data-ttu-id="e7504-118">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e7504-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e7504-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7504-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7504-120">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e7504-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7504-121">CommonParameters</span></span>
<span data-ttu-id="e7504-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7504-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7504-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7504-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7504-124">입력</span><span class="sxs-lookup"><span data-stu-id="e7504-124">INPUTS</span></span>

### <span data-ttu-id="e7504-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e7504-125">System.String</span></span>

## <span data-ttu-id="e7504-126">출력</span><span class="sxs-lookup"><span data-stu-id="e7504-126">OUTPUTS</span></span>

### <span data-ttu-id="e7504-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="e7504-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="e7504-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7504-128">NOTES</span></span>

## <span data-ttu-id="e7504-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7504-129">RELATED LINKS</span></span>

[<span data-ttu-id="e7504-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e7504-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="e7504-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e7504-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="e7504-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="e7504-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
