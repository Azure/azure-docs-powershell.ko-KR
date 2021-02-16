---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0ef2870592411ce64847f8a4a58dabdebcc8235f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408239"
---
# <span data-ttu-id="51ebe-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="51ebe-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="51ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="51ebe-103">ExpressRouteCircuit의 개인 피어링과 연결된 ExpressRoute 회로 연결 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51ebe-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="51ebe-104">구문</span><span class="sxs-lookup"><span data-stu-id="51ebe-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ebe-105">설명</span><span class="sxs-lookup"><span data-stu-id="51ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="51ebe-106">**Get-AzExpressRouteCircuitConnectionConfig** cmdlet은 ExpressRoute 회로에 대한 개인 피어링과 연결된 회로 연결의 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="51ebe-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="51ebe-107">예제</span><span class="sxs-lookup"><span data-stu-id="51ebe-107">EXAMPLES</span></span>

### <span data-ttu-id="51ebe-108">예제 1: ExpressRoute 회로에 대한 회로 연결 구성 표시</span><span class="sxs-lookup"><span data-stu-id="51ebe-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="51ebe-109">예제 2: 파이핑을 사용하여 ExpressRoute 회로와 연결된 회로 연결 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="51ebe-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="51ebe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51ebe-110">PARAMETERS</span></span>

### <span data-ttu-id="51ebe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ebe-111">-DefaultProfile</span></span>
<span data-ttu-id="51ebe-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51ebe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51ebe-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ebe-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="51ebe-114">회로 연결 구성을 포함하는 ExpressRoute 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="51ebe-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="51ebe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="51ebe-115">-Name</span></span>
<span data-ttu-id="51ebe-116">검색할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51ebe-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="51ebe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ebe-117">CommonParameters</span></span>
<span data-ttu-id="51ebe-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51ebe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ebe-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51ebe-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ebe-120">입력</span><span class="sxs-lookup"><span data-stu-id="51ebe-120">INPUTS</span></span>

### <span data-ttu-id="51ebe-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ebe-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="51ebe-122">출력</span><span class="sxs-lookup"><span data-stu-id="51ebe-122">OUTPUTS</span></span>

### <span data-ttu-id="51ebe-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="51ebe-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="51ebe-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51ebe-124">NOTES</span></span>

## <span data-ttu-id="51ebe-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51ebe-125">RELATED LINKS</span></span>

[<span data-ttu-id="51ebe-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51ebe-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="51ebe-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="51ebe-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="51ebe-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="51ebe-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="51ebe-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="51ebe-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)


