---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532220"
---
# <span data-ttu-id="4b911-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b911-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="4b911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b911-102">SYNOPSIS</span></span>
<span data-ttu-id="4b911-103">기본 배포 모델에서 리소스 관리자 배포 모델로 Express 경로를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b911-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b911-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b911-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b911-105">DESCRIPTION</span></span>
<span data-ttu-id="4b911-106">**AzureRmExpressRouteCircuit** cmdlet은 기본 배포 모델에서 리소스 관리자 배포 모델로의 express 경로 회로를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="4b911-107">이동 후에는 () Express 회로가 작동 하 고 리소스 관리자 배포 모델에서 생성 되는 다른 모든 Express 회로와 같이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="4b911-108">회로 링크, 가상 네트워크 및 VPN 게이트웨이는이 작업을 통해 이동 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="4b911-109">이동한 후에는 해당 리소스를 다시 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="4b911-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4b911-110">EXAMPLES</span></span>

### <span data-ttu-id="4b911-111">예제 1: Express 경로 회로를 리소스 관리자 배포 모델로 이동</span><span class="sxs-lookup"><span data-stu-id="4b911-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="4b911-112">변수</span><span class="sxs-lookup"><span data-stu-id="4b911-112">PARAMETERS</span></span>

### <span data-ttu-id="4b911-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4b911-113">-Force</span></span>
<span data-ttu-id="4b911-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b911-115">-위치</span><span class="sxs-lookup"><span data-stu-id="4b911-115">-Location</span></span>
<span data-ttu-id="4b911-116">Express 경로 회로가 있는 Azure 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="4b911-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4b911-117">-Name</span></span>
<span data-ttu-id="4b911-118">이동할 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="4b911-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b911-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b911-120">이동할 대상 회로가 포함 될 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="4b911-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="4b911-121">-ServiceKey</span></span>
<span data-ttu-id="4b911-122">클래식 배포 모델의 Express 경로 회로에서 사용 하는 서비스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="4b911-123">태그</span><span class="sxs-lookup"><span data-stu-id="4b911-123">-Tag</span></span>
<span data-ttu-id="4b911-124">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4b911-125">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="4b911-125">For example:</span></span>

<span data-ttu-id="4b911-126">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4b911-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4b911-127">-확인</span><span class="sxs-lookup"><span data-stu-id="4b911-127">-Confirm</span></span>
<span data-ttu-id="4b911-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b911-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b911-129">-WhatIf</span></span>
<span data-ttu-id="4b911-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b911-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b911-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b911-132">-DefaultProfile</span></span>
<span data-ttu-id="4b911-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b911-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b911-134">CommonParameters</span></span>
<span data-ttu-id="4b911-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b911-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b911-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b911-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b911-137">입력</span><span class="sxs-lookup"><span data-stu-id="4b911-137">INPUTS</span></span>

## <span data-ttu-id="4b911-138">출력</span><span class="sxs-lookup"><span data-stu-id="4b911-138">OUTPUTS</span></span>

### <span data-ttu-id="4b911-139">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4b911-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4b911-140">상속자</span><span class="sxs-lookup"><span data-stu-id="4b911-140">NOTES</span></span>

## <span data-ttu-id="4b911-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b911-141">RELATED LINKS</span></span>

[<span data-ttu-id="4b911-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b911-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4b911-143">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b911-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4b911-144">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b911-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4b911-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4b911-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
