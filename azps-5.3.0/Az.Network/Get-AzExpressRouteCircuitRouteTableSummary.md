---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489939"
---
# <span data-ttu-id="1cbca-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1cbca-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="1cbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cbca-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbca-103">ExpressRoute 회로의 경로 테이블 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1cbca-104">구문</span><span class="sxs-lookup"><span data-stu-id="1cbca-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cbca-105">설명</span><span class="sxs-lookup"><span data-stu-id="1cbca-105">DESCRIPTION</span></span>
<span data-ttu-id="1cbca-106">**Get-AzExpressRouteCircuitRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대한 BGP 인접 정보의 요약을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="1cbca-107">이 정보는 라우팅 컨텍스트가 설정되는 기간 및 피어링 라우터에서 보급하는 경로 연결의 수를 결정하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="1cbca-108">예제</span><span class="sxs-lookup"><span data-stu-id="1cbca-108">EXAMPLES</span></span>

### <span data-ttu-id="1cbca-109">예제 1: 기본 경로에 대한 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="1cbca-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="1cbca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cbca-110">PARAMETERS</span></span>

### <span data-ttu-id="1cbca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbca-111">-DefaultProfile</span></span>
<span data-ttu-id="1cbca-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cbca-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1cbca-113">-DevicePath</span></span>
<span data-ttu-id="1cbca-114">이 매개 변수에 허용되는 값은 `Primary``Secondary`</span><span class="sxs-lookup"><span data-stu-id="1cbca-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="1cbca-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="1cbca-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="1cbca-116">검사할 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="1cbca-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1cbca-117">-PeeringType</span></span>
<span data-ttu-id="1cbca-118">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1cbca-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1cbca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbca-119">-ResourceGroupName</span></span>
<span data-ttu-id="1cbca-120">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="1cbca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbca-121">CommonParameters</span></span>
<span data-ttu-id="1cbca-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1cbca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbca-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cbca-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbca-124">입력</span><span class="sxs-lookup"><span data-stu-id="1cbca-124">INPUTS</span></span>

### <span data-ttu-id="1cbca-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1cbca-125">System.String</span></span>

## <span data-ttu-id="1cbca-126">출력</span><span class="sxs-lookup"><span data-stu-id="1cbca-126">OUTPUTS</span></span>

### <span data-ttu-id="1cbca-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="1cbca-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="1cbca-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1cbca-128">NOTES</span></span>

## <span data-ttu-id="1cbca-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cbca-129">RELATED LINKS</span></span>

[<span data-ttu-id="1cbca-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1cbca-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1cbca-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1cbca-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1cbca-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="1cbca-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
