---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c596dffcef97dfbb1cabbc5ca2c2455a7768c25f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409939"
---
# <span data-ttu-id="5f6df-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f6df-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="5f6df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f6df-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6df-103">ExpressRoute 회로 연결 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="5f6df-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f6df-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f6df-105">설명</span><span class="sxs-lookup"><span data-stu-id="5f6df-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6df-106">**Remove-AzExpressRouteCircuitConnectionConfig** cmdlet은 주어진 ExpressRoute 회로와 연결된 ExpressRoute 회로 연결 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="5f6df-107">예제</span><span class="sxs-lookup"><span data-stu-id="5f6df-107">EXAMPLES</span></span>

### <span data-ttu-id="5f6df-108">예제 1: ExpressRoute 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5f6df-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5f6df-109">예제 2: ExpressRoute 회로에서 Piping을 사용하여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5f6df-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="5f6df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f6df-110">PARAMETERS</span></span>

### <span data-ttu-id="5f6df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6df-111">-DefaultProfile</span></span>
<span data-ttu-id="5f6df-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f6df-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f6df-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5f6df-114">제거할 피어링 구성을 포함하는 ExpressRoute 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="5f6df-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5f6df-115">-Name</span></span>
<span data-ttu-id="5f6df-116">제거할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="5f6df-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f6df-117">-Confirm</span></span>
<span data-ttu-id="5f6df-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6df-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6df-119">-WhatIf</span></span>
<span data-ttu-id="5f6df-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5f6df-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f6df-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6df-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6df-122">CommonParameters</span></span>
<span data-ttu-id="5f6df-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f6df-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6df-124">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5f6df-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6df-125">입력</span><span class="sxs-lookup"><span data-stu-id="5f6df-125">INPUTS</span></span>

### <span data-ttu-id="5f6df-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f6df-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5f6df-127">출력</span><span class="sxs-lookup"><span data-stu-id="5f6df-127">OUTPUTS</span></span>

### <span data-ttu-id="5f6df-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f6df-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5f6df-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f6df-129">NOTES</span></span>

## <span data-ttu-id="5f6df-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f6df-130">RELATED LINKS</span></span>

[<span data-ttu-id="5f6df-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f6df-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5f6df-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f6df-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5f6df-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f6df-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="5f6df-134">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f6df-134">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="5f6df-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f6df-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
