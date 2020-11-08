---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218346"
---
# <span data-ttu-id="91587-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="91587-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="91587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91587-102">SYNOPSIS</span></span>
<span data-ttu-id="91587-103">Express 경로 회로의 사용 통계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91587-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="91587-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91587-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91587-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91587-105">DESCRIPTION</span></span>
<span data-ttu-id="91587-106">**AzExpressRouteCircuitStat** Cmdlet은 express 경로 회로에 대 한 트래픽 통계를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="91587-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="91587-107">통계에는 기본 및 보조 경로를 통해 주고 받은 바이트 수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91587-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="91587-108">예제의</span><span class="sxs-lookup"><span data-stu-id="91587-108">EXAMPLES</span></span>

### <span data-ttu-id="91587-109">예제 1: Express 경로 피어에 대 한 트래픽 통계 표시</span><span class="sxs-lookup"><span data-stu-id="91587-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="91587-110">변수</span><span class="sxs-lookup"><span data-stu-id="91587-110">PARAMETERS</span></span>

### <span data-ttu-id="91587-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91587-111">-DefaultProfile</span></span>
<span data-ttu-id="91587-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91587-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91587-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="91587-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="91587-114">검사 되는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91587-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="91587-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="91587-115">-PeeringType</span></span>
<span data-ttu-id="91587-116">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="91587-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="91587-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91587-117">-ResourceGroupName</span></span>
<span data-ttu-id="91587-118">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91587-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="91587-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91587-119">CommonParameters</span></span>
<span data-ttu-id="91587-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91587-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91587-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91587-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91587-122">입력</span><span class="sxs-lookup"><span data-stu-id="91587-122">INPUTS</span></span>

### <span data-ttu-id="91587-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91587-123">System.String</span></span>

## <span data-ttu-id="91587-124">출력</span><span class="sxs-lookup"><span data-stu-id="91587-124">OUTPUTS</span></span>

### <span data-ttu-id="91587-125">PSExpressRouteCircuitStats에 대 한.</span><span class="sxs-lookup"><span data-stu-id="91587-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="91587-126">상속자</span><span class="sxs-lookup"><span data-stu-id="91587-126">NOTES</span></span>

## <span data-ttu-id="91587-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91587-127">RELATED LINKS</span></span>

[<span data-ttu-id="91587-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="91587-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="91587-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="91587-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="91587-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="91587-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
