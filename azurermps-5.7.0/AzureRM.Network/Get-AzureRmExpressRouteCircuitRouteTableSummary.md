---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 849fb653308537a3d37740a21ba8b488903406ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531022"
---
# <span data-ttu-id="1ed39-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1ed39-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="1ed39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed39-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed39-103">Express 경로 회로에 대 한 라우트 테이블 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed39-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ed39-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ed39-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1ed39-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed39-106">**AzureRmExpressRouteCircuitRouteTableSummary** cmdlet은 특정 라우팅 컨텍스트에 대 한 BGP 인접 정보 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="1ed39-107">이 정보는 라우팅 컨텍스트가 설정 된 시간과 피어 링 라우터에서 알린 경로 접두사의 수를 확인 하는 데 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="1ed39-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1ed39-108">EXAMPLES</span></span>

### <span data-ttu-id="1ed39-109">예제 1: 기본 경로의 경로 요약 표시</span><span class="sxs-lookup"><span data-stu-id="1ed39-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="1ed39-110">변수</span><span class="sxs-lookup"><span data-stu-id="1ed39-110">PARAMETERS</span></span>

### <span data-ttu-id="1ed39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed39-111">-DefaultProfile</span></span>
<span data-ttu-id="1ed39-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed39-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="1ed39-113">-DevicePath</span></span>
<span data-ttu-id="1ed39-114">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="1ed39-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed39-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="1ed39-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="1ed39-116">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed39-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1ed39-117">-PeeringType</span></span>
<span data-ttu-id="1ed39-118">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1ed39-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed39-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed39-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ed39-120">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed39-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed39-121">CommonParameters</span></span>
<span data-ttu-id="1ed39-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed39-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed39-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed39-124">입력</span><span class="sxs-lookup"><span data-stu-id="1ed39-124">INPUTS</span></span>

### <span data-ttu-id="1ed39-125">않아야</span><span class="sxs-lookup"><span data-stu-id="1ed39-125">None</span></span>
<span data-ttu-id="1ed39-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ed39-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ed39-127">출력</span><span class="sxs-lookup"><span data-stu-id="1ed39-127">OUTPUTS</span></span>

### <span data-ttu-id="1ed39-128">PSExpressRouteCircuitRoutesTableSummary에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1ed39-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="1ed39-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1ed39-129">NOTES</span></span>

## <span data-ttu-id="1ed39-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ed39-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ed39-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1ed39-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1ed39-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1ed39-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1ed39-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="1ed39-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
