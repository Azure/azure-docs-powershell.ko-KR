---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: d5b6d1b9e5d3955b7ecbff9dec02405e030bbf33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979595"
---
# <span data-ttu-id="06d06-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="06d06-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="06d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d06-102">SYNOPSIS</span></span>
<span data-ttu-id="06d06-103">ExpressRoute 교차 연결의 경로 테이블 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="06d06-104">구문</span><span class="sxs-lookup"><span data-stu-id="06d06-104">SYNTAX</span></span>

### <span data-ttu-id="06d06-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="06d06-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06d06-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="06d06-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06d06-107">설명</span><span class="sxs-lookup"><span data-stu-id="06d06-107">DESCRIPTION</span></span>
<span data-ttu-id="06d06-108">**Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대한 BGP 인접 정보 요약을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="06d06-109">이 정보는 라우팅 컨텍스트가 설정된 기간 및 피어링 라우터에서 보급하는 경로의 수를 결정하는 데 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="06d06-110">예제</span><span class="sxs-lookup"><span data-stu-id="06d06-110">EXAMPLES</span></span>

### <span data-ttu-id="06d06-111">예제 1: 기본 경로에 대한 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="06d06-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="06d06-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="06d06-112">PARAMETERS</span></span>

### <span data-ttu-id="06d06-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="06d06-113">-CrossConnectionName</span></span>
<span data-ttu-id="06d06-114">Express Route Cross Connection의 이름</span><span class="sxs-lookup"><span data-stu-id="06d06-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="06d06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d06-115">-DefaultProfile</span></span>
<span data-ttu-id="06d06-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d06-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="06d06-117">-DevicePath</span></span>
<span data-ttu-id="06d06-118">이 매개 변수에 대해 허용되는 값은 다음 `Primary` 또는 `Secondary`</span><span class="sxs-lookup"><span data-stu-id="06d06-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="06d06-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="06d06-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="06d06-120">Express 경로 교차 연결</span><span class="sxs-lookup"><span data-stu-id="06d06-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="06d06-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="06d06-121">-PeeringType</span></span>
<span data-ttu-id="06d06-122">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="06d06-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="06d06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d06-123">-ResourceGroupName</span></span>
<span data-ttu-id="06d06-124">ExpressRoute 교차 연결을 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="06d06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d06-125">CommonParameters</span></span>
<span data-ttu-id="06d06-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d06-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06d06-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d06-128">입력</span><span class="sxs-lookup"><span data-stu-id="06d06-128">INPUTS</span></span>

### <span data-ttu-id="06d06-129">없음</span><span class="sxs-lookup"><span data-stu-id="06d06-129">None</span></span>
<span data-ttu-id="06d06-130">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06d06-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06d06-131">출력</span><span class="sxs-lookup"><span data-stu-id="06d06-131">OUTPUTS</span></span>

### <span data-ttu-id="06d06-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="06d06-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="06d06-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06d06-133">NOTES</span></span>

## <span data-ttu-id="06d06-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06d06-134">RELATED LINKS</span></span>

[<span data-ttu-id="06d06-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="06d06-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="06d06-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="06d06-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
