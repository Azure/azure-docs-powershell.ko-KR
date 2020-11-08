---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: b01e0ecb48a5a4c27fc79448ca0e4d71e820d292
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044068"
---
# <span data-ttu-id="f60d3-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f60d3-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f60d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f60d3-103">Express 경로 회로 연결 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="f60d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f60d3-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f60d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f60d3-106">**AzExpressRouteCircuitConnectionConfig** cmdlet은 지정 된 Express 경로 회로와 연결 된 express 회로 연결 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="f60d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f60d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f60d3-108">예제 1: Express 회로에서 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f60d3-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f60d3-109">예제 2: Express 회로에서 파이핑을 사용 하 여 회로 연결 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f60d3-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="f60d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="f60d3-110">PARAMETERS</span></span>

### <span data-ttu-id="f60d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60d3-111">-DefaultProfile</span></span>
<span data-ttu-id="f60d3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f60d3-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f60d3-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f60d3-114">제거할 피어 링 구성을 포함 하는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="f60d3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f60d3-115">-Name</span></span>
<span data-ttu-id="f60d3-116">제거할 회로 연결 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="f60d3-117">-확인</span><span class="sxs-lookup"><span data-stu-id="f60d3-117">-Confirm</span></span>
<span data-ttu-id="f60d3-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60d3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60d3-119">-WhatIf</span></span>
<span data-ttu-id="f60d3-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f60d3-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60d3-122">CommonParameters</span></span>
<span data-ttu-id="f60d3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60d3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60d3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60d3-125">입력</span><span class="sxs-lookup"><span data-stu-id="f60d3-125">INPUTS</span></span>

### <span data-ttu-id="f60d3-126">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f60d3-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f60d3-127">출력</span><span class="sxs-lookup"><span data-stu-id="f60d3-127">OUTPUTS</span></span>

### <span data-ttu-id="f60d3-128">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f60d3-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f60d3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="f60d3-129">NOTES</span></span>

## <span data-ttu-id="f60d3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f60d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="f60d3-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f60d3-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="f60d3-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f60d3-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f60d3-133">추가-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f60d3-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f60d3-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f60d3-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f60d3-135">새로운 AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f60d3-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f60d3-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f60d3-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="f60d3-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f60d3-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)