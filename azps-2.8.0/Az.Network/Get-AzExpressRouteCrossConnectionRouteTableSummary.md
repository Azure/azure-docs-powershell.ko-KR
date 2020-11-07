---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 5e0d9140e11ead75a1abbf43d520d44cffaf5463
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870714"
---
# <span data-ttu-id="8ccea-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ccea-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="8ccea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ccea-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccea-103">Express 간 교차 연결의 경로 테이블 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8ccea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ccea-104">SYNTAX</span></span>

### <span data-ttu-id="8ccea-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="8ccea-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ccea-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="8ccea-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ccea-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8ccea-107">DESCRIPTION</span></span>
<span data-ttu-id="8ccea-108">**AzExpressRouteCrossConnectionRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대 한 BGP 인접 정보 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="8ccea-109">이 정보는 라우팅 컨텍스트가 설정 된 시간과 피어 링 라우터에서 알린 경로 접두사의 수를 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="8ccea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8ccea-110">EXAMPLES</span></span>

### <span data-ttu-id="8ccea-111">예제 1: 기본 경로의 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="8ccea-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="8ccea-112">변수</span><span class="sxs-lookup"><span data-stu-id="8ccea-112">PARAMETERS</span></span>

### <span data-ttu-id="8ccea-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="8ccea-113">-CrossConnectionName</span></span>
<span data-ttu-id="8ccea-114">Express 경로의 이름 교차 연결</span><span class="sxs-lookup"><span data-stu-id="8ccea-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="8ccea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccea-115">-DefaultProfile</span></span>
<span data-ttu-id="8ccea-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ccea-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="8ccea-117">-DevicePath</span></span>
<span data-ttu-id="8ccea-118">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8ccea-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8ccea-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8ccea-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8ccea-120">Express 경로 교차 연결</span><span class="sxs-lookup"><span data-stu-id="8ccea-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="8ccea-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8ccea-121">-PeeringType</span></span>
<span data-ttu-id="8ccea-122">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8ccea-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8ccea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ccea-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ccea-124">Express 경로 간 연결을 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="8ccea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccea-125">CommonParameters</span></span>
<span data-ttu-id="8ccea-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccea-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ccea-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccea-128">입력</span><span class="sxs-lookup"><span data-stu-id="8ccea-128">INPUTS</span></span>

### <span data-ttu-id="8ccea-129">않아야</span><span class="sxs-lookup"><span data-stu-id="8ccea-129">None</span></span>
<span data-ttu-id="8ccea-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ccea-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ccea-131">출력</span><span class="sxs-lookup"><span data-stu-id="8ccea-131">OUTPUTS</span></span>

### <span data-ttu-id="8ccea-132">PSExpressRouteCrossConnectionRoutesTableSummary에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8ccea-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="8ccea-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8ccea-133">NOTES</span></span>

## <span data-ttu-id="8ccea-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ccea-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ccea-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="8ccea-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="8ccea-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ccea-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
