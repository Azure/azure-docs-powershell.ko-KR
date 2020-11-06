---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536599"
---
# <span data-ttu-id="8b447-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8b447-101">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="8b447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b447-102">SYNOPSIS</span></span>
<span data-ttu-id="8b447-103">ExpressRouteCircuit의 개인 피어 링과 연결 된 Express 회로 연결 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b447-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b447-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b447-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b447-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8b447-105">DESCRIPTION</span></span>
<span data-ttu-id="8b447-106">**AzureRmExpressRouteCircuitConnectionConfig** Cmdlet은 express 경로 회로의 개인 피어 링과 연결 된 회로 연결의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b447-106">The **Get-AzureRmExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8b447-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8b447-107">EXAMPLES</span></span>

### <span data-ttu-id="8b447-108">예제 1: Express 경로 회로에 대 한 회로 연결 구성 표시</span><span class="sxs-lookup"><span data-stu-id="8b447-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="8b447-109">예제 2: 파이핑을 사용 하 여 Express 경로 회로와 연결 된 회로 연결 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b447-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="8b447-110">변수</span><span class="sxs-lookup"><span data-stu-id="8b447-110">PARAMETERS</span></span>

### <span data-ttu-id="8b447-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b447-111">-DefaultProfile</span></span>
<span data-ttu-id="8b447-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b447-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b447-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8b447-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8b447-114">회로 연결 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b447-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b447-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8b447-115">-Name</span></span>
<span data-ttu-id="8b447-116">검색할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b447-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b447-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b447-117">CommonParameters</span></span>
<span data-ttu-id="8b447-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b447-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b447-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b447-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b447-120">입력</span><span class="sxs-lookup"><span data-stu-id="8b447-120">INPUTS</span></span>

### <span data-ttu-id="8b447-121">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8b447-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="8b447-122">매개 변수: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8b447-122">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="8b447-123">출력</span><span class="sxs-lookup"><span data-stu-id="8b447-123">OUTPUTS</span></span>

### <span data-ttu-id="8b447-124">PSExpressRouteCircuitConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8b447-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="8b447-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8b447-125">NOTES</span></span>

## <span data-ttu-id="8b447-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b447-126">RELATED LINKS</span></span>

[<span data-ttu-id="8b447-127">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8b447-127">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8b447-128">추가-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8b447-128">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8b447-129">제거-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8b447-129">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8b447-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8b447-130">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8b447-131">새로운 AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8b447-131">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)
