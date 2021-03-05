---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c8d35373c2891b9f0d3ac76ded8b4e9808f32f33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993818"
---
# <span data-ttu-id="b7ec9-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7ec9-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="b7ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ec9-103">ExpressRouteCircuit의 개인 피어링과 연결된 ExpressRoute 회로 연결 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="b7ec9-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7ec9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ec9-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ec9-106">**Get-AzExpressRouteCircuitConnectionConfig** cmdlet은 ExpressRoute 회로에 대한 개인 피어링과 연결된 회로 연결 구성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b7ec9-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ec9-108">예제 1: ExpressRoute 회로에 대한 회로 연결 구성 표시</span><span class="sxs-lookup"><span data-stu-id="b7ec9-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="b7ec9-109">예제 2: 배관을 사용하여 ExpressRoute 회로와 연결된 회로 연결 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="b7ec9-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="b7ec9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7ec9-110">PARAMETERS</span></span>

### <span data-ttu-id="b7ec9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ec9-111">-DefaultProfile</span></span>
<span data-ttu-id="b7ec9-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7ec9-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7ec9-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b7ec9-114">회로 연결 구성을 포함하는 ExpressRoute 회로 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

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

### <span data-ttu-id="b7ec9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ec9-115">-Name</span></span>
<span data-ttu-id="b7ec9-116">검색할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-116">The name of the circuit connection configuration to be retrieved.</span></span>

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

### <span data-ttu-id="b7ec9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ec9-117">CommonParameters</span></span>
<span data-ttu-id="b7ec9-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ec9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ec9-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ec9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ec9-120">입력</span><span class="sxs-lookup"><span data-stu-id="b7ec9-120">INPUTS</span></span>

### <span data-ttu-id="b7ec9-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7ec9-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b7ec9-122">출력</span><span class="sxs-lookup"><span data-stu-id="b7ec9-122">OUTPUTS</span></span>

### <span data-ttu-id="b7ec9-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="b7ec9-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="b7ec9-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7ec9-124">NOTES</span></span>

## <span data-ttu-id="b7ec9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7ec9-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7ec9-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7ec9-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7ec9-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7ec9-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7ec9-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7ec9-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7ec9-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7ec9-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7ec9-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7ec9-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)