---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881397"
---
# <span data-ttu-id="e208c-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e208c-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e208c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e208c-102">SYNOPSIS</span></span>
<span data-ttu-id="e208c-103">기본 배포 모델에서 리소스 관리자 배포 모델로 Express 경로를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e208c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e208c-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e208c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e208c-105">DESCRIPTION</span></span>
<span data-ttu-id="e208c-106">**AzureRmExpressRouteCircuit** cmdlet은 기본 배포 모델에서 리소스 관리자 배포 모델로의 express 경로 회로를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="e208c-107">이동 후에는 () Express 회로가 작동 하 고 리소스 관리자 배포 모델에서 생성 되는 다른 모든 Express 회로와 같이 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="e208c-108">회로 링크, 가상 네트워크 및 VPN 게이트웨이는이 작업을 통해 이동 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="e208c-109">이동한 후에는 해당 리소스를 다시 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="e208c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e208c-110">EXAMPLES</span></span>

### <span data-ttu-id="e208c-111">예제 1: Express 경로 회로를 리소스 관리자 배포 모델로 이동</span><span class="sxs-lookup"><span data-stu-id="e208c-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="e208c-112">변수</span><span class="sxs-lookup"><span data-stu-id="e208c-112">PARAMETERS</span></span>

### <span data-ttu-id="e208c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e208c-113">-AsJob</span></span>
<span data-ttu-id="e208c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e208c-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e208c-115">-DefaultProfile</span></span>
<span data-ttu-id="e208c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e208c-117">-Force</span></span>
<span data-ttu-id="e208c-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-119">-위치</span><span class="sxs-lookup"><span data-stu-id="e208c-119">-Location</span></span>
<span data-ttu-id="e208c-120">Express 경로 회로가 있는 Azure 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e208c-121">-Name</span></span>
<span data-ttu-id="e208c-122">이동할 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e208c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e208c-124">이동할 대상 회로가 포함 될 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="e208c-125">-ServiceKey</span></span>
<span data-ttu-id="e208c-126">클래식 배포 모델의 Express 경로 회로에서 사용 하는 서비스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-127">태그</span><span class="sxs-lookup"><span data-stu-id="e208c-127">-Tag</span></span>
<span data-ttu-id="e208c-128">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e208c-129">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e208c-129">For example:</span></span>

<span data-ttu-id="e208c-130">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e208c-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e208c-131">-Confirm</span></span>
<span data-ttu-id="e208c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e208c-133">-WhatIf</span></span>
<span data-ttu-id="e208c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e208c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e208c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e208c-136">CommonParameters</span></span>
<span data-ttu-id="e208c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e208c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e208c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e208c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e208c-139">입력</span><span class="sxs-lookup"><span data-stu-id="e208c-139">INPUTS</span></span>

## <span data-ttu-id="e208c-140">출력</span><span class="sxs-lookup"><span data-stu-id="e208c-140">OUTPUTS</span></span>

### <span data-ttu-id="e208c-141">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e208c-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e208c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e208c-142">NOTES</span></span>

## <span data-ttu-id="e208c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e208c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e208c-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e208c-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e208c-145">새로운 AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e208c-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e208c-146">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e208c-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e208c-147">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e208c-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
