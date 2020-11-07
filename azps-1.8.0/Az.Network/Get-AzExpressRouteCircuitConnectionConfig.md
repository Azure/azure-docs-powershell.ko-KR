---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 70badaebf0b6b8a35fd96cc20a54aab1ff316bef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700601"
---
# <span data-ttu-id="d3587-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d3587-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="d3587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3587-102">SYNOPSIS</span></span>
<span data-ttu-id="d3587-103">ExpressRouteCircuit의 개인 피어 링과 연결 된 Express 회로 연결 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3587-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="d3587-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3587-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3587-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3587-105">DESCRIPTION</span></span>
<span data-ttu-id="d3587-106">**AzExpressRouteCircuitConnectionConfig** Cmdlet은 express 경로 회로의 개인 피어 링과 연결 된 회로 연결의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3587-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d3587-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3587-107">EXAMPLES</span></span>

### <span data-ttu-id="d3587-108">예제 1: Express 경로 회로에 대 한 회로 연결 구성 표시</span><span class="sxs-lookup"><span data-stu-id="d3587-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="d3587-109">예제 2: 파이핑을 사용 하 여 Express 경로 회로와 연결 된 회로 연결 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3587-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="d3587-110">변수</span><span class="sxs-lookup"><span data-stu-id="d3587-110">PARAMETERS</span></span>

### <span data-ttu-id="d3587-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3587-111">-DefaultProfile</span></span>
<span data-ttu-id="d3587-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3587-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3587-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3587-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d3587-114">회로 연결 구성을 포함 하는 Express 경로 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d3587-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="d3587-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d3587-115">-Name</span></span>
<span data-ttu-id="d3587-116">검색할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3587-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3587-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3587-117">CommonParameters</span></span>
<span data-ttu-id="d3587-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3587-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3587-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3587-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3587-120">입력</span><span class="sxs-lookup"><span data-stu-id="d3587-120">INPUTS</span></span>

### <span data-ttu-id="d3587-121">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d3587-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d3587-122">출력</span><span class="sxs-lookup"><span data-stu-id="d3587-122">OUTPUTS</span></span>

### <span data-ttu-id="d3587-123">PSExpressRouteCircuitConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d3587-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="d3587-124">상속자</span><span class="sxs-lookup"><span data-stu-id="d3587-124">NOTES</span></span>

## <span data-ttu-id="d3587-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3587-125">RELATED LINKS</span></span>

[<span data-ttu-id="d3587-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3587-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d3587-127">추가-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d3587-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d3587-128">제거-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d3587-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d3587-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d3587-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d3587-130">새로운 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d3587-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)