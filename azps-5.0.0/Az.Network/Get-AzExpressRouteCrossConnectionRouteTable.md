---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226681"
---
# <span data-ttu-id="3528c-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3528c-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="3528c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3528c-102">SYNOPSIS</span></span>
<span data-ttu-id="3528c-103">Express 간 교차 연결에서 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="3528c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3528c-104">SYNTAX</span></span>

### <span data-ttu-id="3528c-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="3528c-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3528c-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="3528c-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3528c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3528c-107">DESCRIPTION</span></span>
<span data-ttu-id="3528c-108">AzExpressRouteCrossConnectionRouteTable cmdlet은이 ( **가)** express 회로의 상세 경로 테이블을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="3528c-109">경로 테이블에는 모든 경로가 표시 되거나 특정 피어 링 유형에 대 한 경로를 표시 하도록 필터링 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="3528c-110">경로 테이블을 사용 하 여 피어 링 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="3528c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3528c-111">EXAMPLES</span></span>

### <span data-ttu-id="3528c-112">예제 1: 기본 경로의 경로 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="3528c-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="3528c-113">변수</span><span class="sxs-lookup"><span data-stu-id="3528c-113">PARAMETERS</span></span>

### <span data-ttu-id="3528c-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="3528c-114">-CrossConnectionName</span></span>
<span data-ttu-id="3528c-115">Express 경로의 이름 교차 연결</span><span class="sxs-lookup"><span data-stu-id="3528c-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="3528c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3528c-116">-DefaultProfile</span></span>
<span data-ttu-id="3528c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3528c-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="3528c-118">-DevicePath</span></span>
<span data-ttu-id="3528c-119">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="3528c-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="3528c-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3528c-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="3528c-121">Express 경로 교차 연결</span><span class="sxs-lookup"><span data-stu-id="3528c-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="3528c-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3528c-122">-PeeringType</span></span>
<span data-ttu-id="3528c-123">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3528c-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3528c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3528c-124">-ResourceGroupName</span></span>
<span data-ttu-id="3528c-125">Express 경로 간 연결을 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="3528c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3528c-126">CommonParameters</span></span>
<span data-ttu-id="3528c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3528c-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3528c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3528c-129">입력</span><span class="sxs-lookup"><span data-stu-id="3528c-129">INPUTS</span></span>

### <span data-ttu-id="3528c-130">않아야</span><span class="sxs-lookup"><span data-stu-id="3528c-130">None</span></span>
<span data-ttu-id="3528c-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3528c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3528c-132">출력</span><span class="sxs-lookup"><span data-stu-id="3528c-132">OUTPUTS</span></span>

### <span data-ttu-id="3528c-133">PSExpressRouteCircuitRoutesTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3528c-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="3528c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="3528c-134">NOTES</span></span>

## <span data-ttu-id="3528c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3528c-135">RELATED LINKS</span></span>

[<span data-ttu-id="3528c-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="3528c-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="3528c-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3528c-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
