---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529485"
---
# <span data-ttu-id="5fbc4-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fbc4-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="5fbc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbc4-103">Express 경로 회로 연결 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fbc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5fbc4-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbc4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5fbc4-105">DESCRIPTION</span></span>
<span data-ttu-id="5fbc4-106">**AzureRmExpressRouteCircuitConnectionConfig** cmdlet은 지정 된 Express 경로 회로와 연결 된 express 회로 연결 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="5fbc4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5fbc4-107">EXAMPLES</span></span>

### <span data-ttu-id="5fbc4-108">예제 1: Express 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5fbc4-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5fbc4-109">예제 2: Express 회로에서 파이핑을 사용 하 여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5fbc4-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="5fbc4-110">변수</span><span class="sxs-lookup"><span data-stu-id="5fbc4-110">PARAMETERS</span></span>

### <span data-ttu-id="5fbc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbc4-111">-DefaultProfile</span></span>
<span data-ttu-id="5fbc4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fbc4-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fbc4-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5fbc4-114">제거할 피어 링 구성을 포함 하는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="5fbc4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5fbc4-115">-Name</span></span>
<span data-ttu-id="5fbc4-116">제거할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="5fbc4-117">-확인</span><span class="sxs-lookup"><span data-stu-id="5fbc4-117">-Confirm</span></span>
<span data-ttu-id="5fbc4-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbc4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbc4-119">-WhatIf</span></span>
<span data-ttu-id="5fbc4-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fbc4-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fbc4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbc4-122">CommonParameters</span></span>
<span data-ttu-id="5fbc4-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbc4-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbc4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbc4-125">입력</span><span class="sxs-lookup"><span data-stu-id="5fbc4-125">INPUTS</span></span>

### <span data-ttu-id="5fbc4-126">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="5fbc4-127">매개 변수: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5fbc4-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="5fbc4-128">출력</span><span class="sxs-lookup"><span data-stu-id="5fbc4-128">OUTPUTS</span></span>

### <span data-ttu-id="5fbc4-129">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5fbc4-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5fbc4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5fbc4-130">NOTES</span></span>

## <span data-ttu-id="5fbc4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fbc4-131">RELATED LINKS</span></span>

[<span data-ttu-id="5fbc4-132">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fbc4-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5fbc4-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fbc4-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fbc4-134">추가-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fbc4-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fbc4-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fbc4-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fbc4-136">새로운 AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5fbc4-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5fbc4-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fbc4-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="5fbc4-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5fbc4-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
