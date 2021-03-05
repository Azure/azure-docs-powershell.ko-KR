---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997733"
---
# <span data-ttu-id="d2cf5-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="d2cf5-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="d2cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cf5-103">ExpressRoute 회로의 사용 통계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d2cf5-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2cf5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2cf5-105">설명</span><span class="sxs-lookup"><span data-stu-id="d2cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="d2cf5-106">**Get-AzExpressRouteCircuitStat** cmdlet은 ExpressRoute 회로에 대한 트래픽 통계를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="d2cf5-107">통계에는 주 경로와 보조 경로 둘 다를 통해 전송 및 수신된 byte의 수가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="d2cf5-108">예제</span><span class="sxs-lookup"><span data-stu-id="d2cf5-108">EXAMPLES</span></span>

### <span data-ttu-id="d2cf5-109">예제 1: ExpressRoute 피어에 대한 트래픽 통계 표시</span><span class="sxs-lookup"><span data-stu-id="d2cf5-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="d2cf5-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d2cf5-110">PARAMETERS</span></span>

### <span data-ttu-id="d2cf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cf5-111">-DefaultProfile</span></span>
<span data-ttu-id="d2cf5-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2cf5-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d2cf5-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d2cf5-114">검사되는 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="d2cf5-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d2cf5-115">-PeeringType</span></span>
<span data-ttu-id="d2cf5-116">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d2cf5-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2cf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2cf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2cf5-118">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d2cf5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cf5-119">CommonParameters</span></span>
<span data-ttu-id="d2cf5-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2cf5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cf5-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2cf5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cf5-122">입력</span><span class="sxs-lookup"><span data-stu-id="d2cf5-122">INPUTS</span></span>

### <span data-ttu-id="d2cf5-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d2cf5-123">System.String</span></span>

## <span data-ttu-id="d2cf5-124">출력</span><span class="sxs-lookup"><span data-stu-id="d2cf5-124">OUTPUTS</span></span>

### <span data-ttu-id="d2cf5-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="d2cf5-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="d2cf5-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2cf5-126">NOTES</span></span>

## <span data-ttu-id="d2cf5-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2cf5-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2cf5-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d2cf5-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d2cf5-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d2cf5-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="d2cf5-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d2cf5-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
