---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952203"
---
# <span data-ttu-id="77c30-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77c30-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="77c30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77c30-102">SYNOPSIS</span></span>
<span data-ttu-id="77c30-103">클래식 배포 모델에서 Resource Manager 배포 모델로 ExpressRoute 회로를 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="77c30-104">구문</span><span class="sxs-lookup"><span data-stu-id="77c30-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77c30-105">설명</span><span class="sxs-lookup"><span data-stu-id="77c30-105">DESCRIPTION</span></span>
<span data-ttu-id="77c30-106">**Move-AzExpressRouteCircuit** cmdlet은 ExpressRoute 회로를 클래식 배포 모델에서 Resource Manager 배포 모델로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="77c30-107">이동 후 ExpressRoute 회로는 Resource Manager 배포 모델에 생성된 다른 ExpressRoute 회로와 같이 행동하고 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="77c30-108">회로 링크, 가상 네트워크 및 VPN 게이트웨이는 이 작업을 통해 이동되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="77c30-109">이러한 리소스는 이동 후 다시 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="77c30-110">예제</span><span class="sxs-lookup"><span data-stu-id="77c30-110">EXAMPLES</span></span>

### <span data-ttu-id="77c30-111">예제 1: ExpressRoute 회로를 Resource Manager 배포 모델로 이동</span><span class="sxs-lookup"><span data-stu-id="77c30-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="77c30-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="77c30-112">PARAMETERS</span></span>

### <span data-ttu-id="77c30-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77c30-113">-AsJob</span></span>
<span data-ttu-id="77c30-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="77c30-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77c30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c30-115">-DefaultProfile</span></span>
<span data-ttu-id="77c30-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77c30-117">-Force</span><span class="sxs-lookup"><span data-stu-id="77c30-117">-Force</span></span>
<span data-ttu-id="77c30-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77c30-119">-Location</span><span class="sxs-lookup"><span data-stu-id="77c30-119">-Location</span></span>
<span data-ttu-id="77c30-120">ExpressRoute 회로가 있는 Azure 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="77c30-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77c30-121">-Name</span></span>
<span data-ttu-id="77c30-122">이동할 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="77c30-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c30-123">-ResourceGroupName</span></span>
<span data-ttu-id="77c30-124">이동되는 ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="77c30-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="77c30-125">-ServiceKey</span></span>
<span data-ttu-id="77c30-126">클래식 배포 모델의 ExpressRoute 회로에서 사용하는 서비스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="77c30-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="77c30-127">-Tag</span></span>
<span data-ttu-id="77c30-128">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="77c30-129">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="77c30-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="77c30-130">-확인</span><span class="sxs-lookup"><span data-stu-id="77c30-130">-Confirm</span></span>
<span data-ttu-id="77c30-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c30-132">-WhatIf</span></span>
<span data-ttu-id="77c30-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77c30-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c30-135">CommonParameters</span></span>
<span data-ttu-id="77c30-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77c30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c30-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="77c30-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c30-138">입력</span><span class="sxs-lookup"><span data-stu-id="77c30-138">INPUTS</span></span>

### <span data-ttu-id="77c30-139">System.String</span><span class="sxs-lookup"><span data-stu-id="77c30-139">System.String</span></span>

### <span data-ttu-id="77c30-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="77c30-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="77c30-141">출력</span><span class="sxs-lookup"><span data-stu-id="77c30-141">OUTPUTS</span></span>

### <span data-ttu-id="77c30-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77c30-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="77c30-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77c30-143">NOTES</span></span>

## <span data-ttu-id="77c30-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77c30-144">RELATED LINKS</span></span>

[<span data-ttu-id="77c30-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77c30-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="77c30-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77c30-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="77c30-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77c30-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="77c30-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="77c30-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
