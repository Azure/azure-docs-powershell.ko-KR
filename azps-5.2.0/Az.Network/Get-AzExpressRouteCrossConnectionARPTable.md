---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329769"
---
# <span data-ttu-id="f685e-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f685e-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="f685e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f685e-102">SYNOPSIS</span></span>
<span data-ttu-id="f685e-103">ExpressRoute 교차 연결에서 ARP 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="f685e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f685e-104">SYNTAX</span></span>

### <span data-ttu-id="f685e-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="f685e-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f685e-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="f685e-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f685e-107">설명</span><span class="sxs-lookup"><span data-stu-id="f685e-107">DESCRIPTION</span></span>
<span data-ttu-id="f685e-108">**Get-AzExpressRouteCrossConnectionARPTable** cmdlet은 ExpressRoute 교차 연결의 두 인터페이스에서 ARP 테이블을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="f685e-109">ARP 테이블은 특정 피어링에 대한 MAC 주소에 대한 IPv4 주소 매핑을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="f685e-110">ARP 테이블을 사용하여 계층 2 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="f685e-111">예제</span><span class="sxs-lookup"><span data-stu-id="f685e-111">EXAMPLES</span></span>

### <span data-ttu-id="f685e-112">예제 1: ExpressRoute 피어에 대한 ARP 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="f685e-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="f685e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f685e-113">PARAMETERS</span></span>

### <span data-ttu-id="f685e-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="f685e-114">-CrossConnectionName</span></span>
<span data-ttu-id="f685e-115">Express Route 교차 연결의 이름</span><span class="sxs-lookup"><span data-stu-id="f685e-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="f685e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f685e-116">-DefaultProfile</span></span>
<span data-ttu-id="f685e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f685e-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f685e-118">-DevicePath</span></span>
<span data-ttu-id="f685e-119">이 매개 변수에 허용되는 값은 `Primary``Secondary`</span><span class="sxs-lookup"><span data-stu-id="f685e-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f685e-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f685e-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f685e-121">Express Route 교차 연결</span><span class="sxs-lookup"><span data-stu-id="f685e-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="f685e-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f685e-122">-PeeringType</span></span>
<span data-ttu-id="f685e-123">이 매개 변수에 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f685e-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f685e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f685e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f685e-125">ExpressRoute 교차 연결을 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="f685e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f685e-126">CommonParameters</span></span>
<span data-ttu-id="f685e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f685e-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f685e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f685e-129">입력</span><span class="sxs-lookup"><span data-stu-id="f685e-129">INPUTS</span></span>

### <span data-ttu-id="f685e-130">없음</span><span class="sxs-lookup"><span data-stu-id="f685e-130">None</span></span>
<span data-ttu-id="f685e-131">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f685e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f685e-132">출력</span><span class="sxs-lookup"><span data-stu-id="f685e-132">OUTPUTS</span></span>

### <span data-ttu-id="f685e-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="f685e-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="f685e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f685e-134">NOTES</span></span>

## <span data-ttu-id="f685e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f685e-135">RELATED LINKS</span></span>

[<span data-ttu-id="f685e-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f685e-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="f685e-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f685e-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
