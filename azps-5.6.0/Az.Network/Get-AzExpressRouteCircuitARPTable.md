---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: b82ef556db076c46fbfe098ba2c2f76e9abab862
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967856"
---
# <span data-ttu-id="57ddd-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="57ddd-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="57ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="57ddd-103">ExpressRoute 회로에서 ARP 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="57ddd-104">구문</span><span class="sxs-lookup"><span data-stu-id="57ddd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57ddd-105">설명</span><span class="sxs-lookup"><span data-stu-id="57ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="57ddd-106">**Get-AzExpressRouteCircuitARPTable** cmdlet은 ExpressRoute 회로의 두 인터페이스에서 ARP 테이블을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="57ddd-107">ARP 테이블은 특정 피어링에 대한 IPv4 주소를 MAC 주소에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="57ddd-108">ARP 테이블을 사용하여 계층 2 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="57ddd-109">예제</span><span class="sxs-lookup"><span data-stu-id="57ddd-109">EXAMPLES</span></span>

### <span data-ttu-id="57ddd-110">예제 1: ExpressRoute 피어에 대한 ARP 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="57ddd-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="57ddd-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="57ddd-111">PARAMETERS</span></span>

### <span data-ttu-id="57ddd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ddd-112">-DefaultProfile</span></span>
<span data-ttu-id="57ddd-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ddd-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="57ddd-114">-DevicePath</span></span>
<span data-ttu-id="57ddd-115">이 매개 변수에 대해 허용되는 값은 다음 `Primary` 또는 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="57ddd-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="57ddd-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="57ddd-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="57ddd-117">검사되는 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="57ddd-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="57ddd-118">-PeeringType</span></span>
<span data-ttu-id="57ddd-119">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="57ddd-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="57ddd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ddd-120">-ResourceGroupName</span></span>
<span data-ttu-id="57ddd-121">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="57ddd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ddd-122">CommonParameters</span></span>
<span data-ttu-id="57ddd-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57ddd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ddd-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57ddd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ddd-125">입력</span><span class="sxs-lookup"><span data-stu-id="57ddd-125">INPUTS</span></span>

### <span data-ttu-id="57ddd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="57ddd-126">System.String</span></span>

## <span data-ttu-id="57ddd-127">출력</span><span class="sxs-lookup"><span data-stu-id="57ddd-127">OUTPUTS</span></span>

### <span data-ttu-id="57ddd-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="57ddd-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="57ddd-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57ddd-129">NOTES</span></span>

## <span data-ttu-id="57ddd-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57ddd-130">RELATED LINKS</span></span>

[<span data-ttu-id="57ddd-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="57ddd-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="57ddd-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="57ddd-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="57ddd-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="57ddd-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
