---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 4b3f7e455d11696ca92ae8a2e8b530dc8d875123
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408273"
---
# <span data-ttu-id="6a3c1-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6a3c1-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="6a3c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3c1-103">ExpressRoute 회로에서 ARP 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6a3c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a3c1-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a3c1-105">설명</span><span class="sxs-lookup"><span data-stu-id="6a3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3c1-106">**Get-AzExpressRouteCircuitARPTable** cmdlet은 ExpressRoute 회로의 두 인터페이스에서 ARP 테이블을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="6a3c1-107">ARP 테이블은 특정 피어링에 대한 MAC 주소에 대한 IPv4 주소의 매핑을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="6a3c1-108">ARP 테이블을 사용하여 계층 2 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="6a3c1-109">예제</span><span class="sxs-lookup"><span data-stu-id="6a3c1-109">EXAMPLES</span></span>

### <span data-ttu-id="6a3c1-110">예제 1: ExpressRoute 피어에 대한 ARP 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="6a3c1-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="6a3c1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a3c1-111">PARAMETERS</span></span>

### <span data-ttu-id="6a3c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3c1-112">-DefaultProfile</span></span>
<span data-ttu-id="6a3c1-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3c1-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="6a3c1-114">-DevicePath</span></span>
<span data-ttu-id="6a3c1-115">이 매개 변수에 허용되는 값은 `Primary``Secondary`</span><span class="sxs-lookup"><span data-stu-id="6a3c1-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="6a3c1-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="6a3c1-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="6a3c1-117">검사할 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="6a3c1-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6a3c1-118">-PeeringType</span></span>
<span data-ttu-id="6a3c1-119">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6a3c1-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="6a3c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a3c1-121">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6a3c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3c1-122">CommonParameters</span></span>
<span data-ttu-id="6a3c1-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3c1-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a3c1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3c1-125">입력</span><span class="sxs-lookup"><span data-stu-id="6a3c1-125">INPUTS</span></span>

### <span data-ttu-id="6a3c1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6a3c1-126">System.String</span></span>

## <span data-ttu-id="6a3c1-127">출력</span><span class="sxs-lookup"><span data-stu-id="6a3c1-127">OUTPUTS</span></span>

### <span data-ttu-id="6a3c1-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="6a3c1-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="6a3c1-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a3c1-129">NOTES</span></span>

## <span data-ttu-id="6a3c1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a3c1-130">RELATED LINKS</span></span>

[<span data-ttu-id="6a3c1-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6a3c1-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="6a3c1-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6a3c1-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="6a3c1-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="6a3c1-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
