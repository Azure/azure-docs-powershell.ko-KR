---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionArpTable.md
ms.openlocfilehash: 8dac5f65599ead696416eaf33f8773415a5631cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187196"
---
# <span data-ttu-id="f6b63-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f6b63-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="f6b63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b63-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b63-103">ExpressRoute 교차 연결에서 ARP 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="f6b63-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6b63-104">SYNTAX</span></span>

### <span data-ttu-id="f6b63-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="f6b63-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6b63-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="f6b63-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6b63-107">설명</span><span class="sxs-lookup"><span data-stu-id="f6b63-107">DESCRIPTION</span></span>
<span data-ttu-id="f6b63-108">**Get-AzExpressRouteCrossConnectionARPTable** cmdlet은 ExpressRoute 교차 연결의 두 인터페이스에서 ARP 테이블을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="f6b63-109">ARP 테이블은 특정 피어링에 대한 MAC 주소에 대한 IPv4 주소 매핑을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="f6b63-110">ARP 테이블을 사용하여 계층 2 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="f6b63-111">예제</span><span class="sxs-lookup"><span data-stu-id="f6b63-111">EXAMPLES</span></span>

### <span data-ttu-id="f6b63-112">예제 1: ExpressRoute 피어에 대한 ARP 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="f6b63-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="f6b63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6b63-113">PARAMETERS</span></span>

### <span data-ttu-id="f6b63-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="f6b63-114">-CrossConnectionName</span></span>
<span data-ttu-id="f6b63-115">Express Route 교차 연결의 이름</span><span class="sxs-lookup"><span data-stu-id="f6b63-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b63-116">-DefaultProfile</span></span>
<span data-ttu-id="f6b63-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6b63-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f6b63-118">-DevicePath</span></span>
<span data-ttu-id="f6b63-119">이 매개 변수에 허용되는 값은 `Primary``Secondary`</span><span class="sxs-lookup"><span data-stu-id="f6b63-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f6b63-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f6b63-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f6b63-121">Express Route 교차 연결</span><span class="sxs-lookup"><span data-stu-id="f6b63-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b63-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f6b63-122">-PeeringType</span></span>
<span data-ttu-id="f6b63-123">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f6b63-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f6b63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b63-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6b63-125">ExpressRoute 교차 연결을 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b63-126">CommonParameters</span></span>
<span data-ttu-id="f6b63-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b63-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6b63-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b63-129">입력</span><span class="sxs-lookup"><span data-stu-id="f6b63-129">INPUTS</span></span>

### <span data-ttu-id="f6b63-130">없음</span><span class="sxs-lookup"><span data-stu-id="f6b63-130">None</span></span>
<span data-ttu-id="f6b63-131">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b63-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6b63-132">출력</span><span class="sxs-lookup"><span data-stu-id="f6b63-132">OUTPUTS</span></span>

### <span data-ttu-id="f6b63-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="f6b63-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="f6b63-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6b63-134">NOTES</span></span>

## <span data-ttu-id="f6b63-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6b63-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6b63-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f6b63-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="f6b63-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f6b63-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
