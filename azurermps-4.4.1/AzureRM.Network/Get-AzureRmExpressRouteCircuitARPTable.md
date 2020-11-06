---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: e306faae861b8f35bff3695dc4235394764621a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527439"
---
# <span data-ttu-id="67186-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="67186-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="67186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67186-102">SYNOPSIS</span></span>
<span data-ttu-id="67186-103">Express 경로 회로에서 ARP 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67186-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67186-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67186-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67186-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67186-105">DESCRIPTION</span></span>
<span data-ttu-id="67186-106">**AzureRmExpressRouteCircuitARPTable** Cmdlet은 express 경로 회로의 두 인터페이스에서 ARP 테이블을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="67186-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="67186-107">ARP 테이블은 특정 피어 링에 대 한 IPv4 주소를 MAC 주소로 매핑하는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="67186-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="67186-108">ARP 테이블을 사용 하 여 계층 2 구성 및 연결의 유효성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67186-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="67186-109">예제의</span><span class="sxs-lookup"><span data-stu-id="67186-109">EXAMPLES</span></span>

### <span data-ttu-id="67186-110">예제 1: Express 경로 피어에 대 한 ARP 테이블 표시</span><span class="sxs-lookup"><span data-stu-id="67186-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="67186-111">변수</span><span class="sxs-lookup"><span data-stu-id="67186-111">PARAMETERS</span></span>

### <span data-ttu-id="67186-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="67186-112">-DevicePath</span></span>
<span data-ttu-id="67186-113">이 매개 변수에 허용 되는 값은 `Primary` 다음과 같습니다. `Secondary`</span><span class="sxs-lookup"><span data-stu-id="67186-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="67186-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="67186-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="67186-115">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67186-115">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="67186-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="67186-116">-PeeringType</span></span>
<span data-ttu-id="67186-117">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="67186-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="67186-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67186-118">-ResourceGroupName</span></span>
<span data-ttu-id="67186-119">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67186-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="67186-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67186-120">-DefaultProfile</span></span>
<span data-ttu-id="67186-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67186-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67186-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67186-122">CommonParameters</span></span>
<span data-ttu-id="67186-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67186-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67186-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67186-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67186-125">입력</span><span class="sxs-lookup"><span data-stu-id="67186-125">INPUTS</span></span>

## <span data-ttu-id="67186-126">출력</span><span class="sxs-lookup"><span data-stu-id="67186-126">OUTPUTS</span></span>

### <span data-ttu-id="67186-127">PSExpressRouteCircuitArpTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="67186-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="67186-128">상속자</span><span class="sxs-lookup"><span data-stu-id="67186-128">NOTES</span></span>

## <span data-ttu-id="67186-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67186-129">RELATED LINKS</span></span>

[<span data-ttu-id="67186-130">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="67186-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="67186-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="67186-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="67186-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="67186-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
