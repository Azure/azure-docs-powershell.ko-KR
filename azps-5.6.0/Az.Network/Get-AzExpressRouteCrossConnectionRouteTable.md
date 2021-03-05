---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: c92033fa0ed907aab4c36f7dd980fb977a47be73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979600"
---
# <span data-ttu-id="4adbf-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4adbf-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="4adbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4adbf-102">SYNOPSIS</span></span>
<span data-ttu-id="4adbf-103">ExpressRoute 교차 연결에서 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="4adbf-104">구문</span><span class="sxs-lookup"><span data-stu-id="4adbf-104">SYNTAX</span></span>

### <span data-ttu-id="4adbf-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="4adbf-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4adbf-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="4adbf-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4adbf-107">설명</span><span class="sxs-lookup"><span data-stu-id="4adbf-107">DESCRIPTION</span></span>
<span data-ttu-id="4adbf-108">**Get-AzExpressRouteCrossConnectionRouteTable** cmdlet은 ExpressRoute 회로의 자세한 경로 테이블을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="4adbf-109">경로 테이블은 모든 경로를 표시하거나 필터링하여 특정 피어링 유형에 대한 경로를 표시하도록 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="4adbf-110">경로 테이블을 사용하여 피어링 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="4adbf-111">예제</span><span class="sxs-lookup"><span data-stu-id="4adbf-111">EXAMPLES</span></span>

### <span data-ttu-id="4adbf-112">예제 1: 기본 경로에 대한 경로 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="4adbf-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="4adbf-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4adbf-113">PARAMETERS</span></span>

### <span data-ttu-id="4adbf-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="4adbf-114">-CrossConnectionName</span></span>
<span data-ttu-id="4adbf-115">Express Route Cross Connection의 이름</span><span class="sxs-lookup"><span data-stu-id="4adbf-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="4adbf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4adbf-116">-DefaultProfile</span></span>
<span data-ttu-id="4adbf-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4adbf-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="4adbf-118">-DevicePath</span></span>
<span data-ttu-id="4adbf-119">이 매개 변수에 대해 허용되는 값은 다음 `Primary` 또는 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="4adbf-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="4adbf-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4adbf-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="4adbf-121">Express 경로 교차 연결</span><span class="sxs-lookup"><span data-stu-id="4adbf-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="4adbf-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4adbf-122">-PeeringType</span></span>
<span data-ttu-id="4adbf-123">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4adbf-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4adbf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4adbf-124">-ResourceGroupName</span></span>
<span data-ttu-id="4adbf-125">ExpressRoute 교차 연결을 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="4adbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4adbf-126">CommonParameters</span></span>
<span data-ttu-id="4adbf-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4adbf-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4adbf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4adbf-129">입력</span><span class="sxs-lookup"><span data-stu-id="4adbf-129">INPUTS</span></span>

### <span data-ttu-id="4adbf-130">없음</span><span class="sxs-lookup"><span data-stu-id="4adbf-130">None</span></span>
<span data-ttu-id="4adbf-131">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4adbf-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4adbf-132">출력</span><span class="sxs-lookup"><span data-stu-id="4adbf-132">OUTPUTS</span></span>

### <span data-ttu-id="4adbf-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="4adbf-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="4adbf-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4adbf-134">NOTES</span></span>

## <span data-ttu-id="4adbf-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4adbf-135">RELATED LINKS</span></span>

[<span data-ttu-id="4adbf-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="4adbf-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="4adbf-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4adbf-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
