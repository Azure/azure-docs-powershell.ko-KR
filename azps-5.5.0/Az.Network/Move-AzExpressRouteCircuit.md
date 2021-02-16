---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191889"
---
# <span data-ttu-id="40483-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="40483-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="40483-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40483-102">SYNOPSIS</span></span>
<span data-ttu-id="40483-103">클래식 배포 모델에서 Resource Manager 배포 모델로 ExpressRoute 회로를 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="40483-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="40483-104">구문</span><span class="sxs-lookup"><span data-stu-id="40483-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40483-105">설명</span><span class="sxs-lookup"><span data-stu-id="40483-105">DESCRIPTION</span></span>
<span data-ttu-id="40483-106">**Move-AzExpressRouteCircuit** cmdlet은 클래식 배포 모델에서 Resource Manager 배포 모델로 ExpressRoute 회로를 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="40483-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="40483-107">이동 후 ExpressRoute 회로는 Resource Manager 배포 모델에서 만든 다른 ExpressRoute 회로처럼 행동하고 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="40483-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="40483-108">회로 링크, 가상 네트워크 및 VPN 게이트웨이는 이 작업을 통해 이동되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40483-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="40483-109">이러한 리소스는 이동 후에 다시 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40483-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="40483-110">예제</span><span class="sxs-lookup"><span data-stu-id="40483-110">EXAMPLES</span></span>

### <span data-ttu-id="40483-111">예제 1: ExpressRoute 회로를 Resource Manager 배포 모델로 이동</span><span class="sxs-lookup"><span data-stu-id="40483-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="40483-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40483-112">PARAMETERS</span></span>

### <span data-ttu-id="40483-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40483-113">-AsJob</span></span>
<span data-ttu-id="40483-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="40483-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40483-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40483-115">-DefaultProfile</span></span>
<span data-ttu-id="40483-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40483-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40483-117">-Force</span><span class="sxs-lookup"><span data-stu-id="40483-117">-Force</span></span>
<span data-ttu-id="40483-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="40483-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40483-119">-Location</span><span class="sxs-lookup"><span data-stu-id="40483-119">-Location</span></span>
<span data-ttu-id="40483-120">ExpressRoute 회로가 있는 Azure 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40483-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="40483-121">-Name</span><span class="sxs-lookup"><span data-stu-id="40483-121">-Name</span></span>
<span data-ttu-id="40483-122">이동할 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40483-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40483-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40483-123">-ResourceGroupName</span></span>
<span data-ttu-id="40483-124">이동되는 ExpressRoute 회로를 포함할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40483-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="40483-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="40483-125">-ServiceKey</span></span>
<span data-ttu-id="40483-126">클래식 배포 모델의 ExpressRoute 회로에서 사용하는 서비스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="40483-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="40483-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="40483-127">-Tag</span></span>
<span data-ttu-id="40483-128">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="40483-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40483-129">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="40483-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40483-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40483-130">-Confirm</span></span>
<span data-ttu-id="40483-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40483-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40483-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40483-132">-WhatIf</span></span>
<span data-ttu-id="40483-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="40483-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40483-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40483-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40483-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40483-135">CommonParameters</span></span>
<span data-ttu-id="40483-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40483-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40483-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="40483-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40483-138">입력</span><span class="sxs-lookup"><span data-stu-id="40483-138">INPUTS</span></span>

### <span data-ttu-id="40483-139">System.String</span><span class="sxs-lookup"><span data-stu-id="40483-139">System.String</span></span>

### <span data-ttu-id="40483-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="40483-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="40483-141">출력</span><span class="sxs-lookup"><span data-stu-id="40483-141">OUTPUTS</span></span>

### <span data-ttu-id="40483-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="40483-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="40483-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40483-143">NOTES</span></span>

## <span data-ttu-id="40483-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40483-144">RELATED LINKS</span></span>

[<span data-ttu-id="40483-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="40483-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="40483-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="40483-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="40483-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="40483-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="40483-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="40483-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
