---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: 0b4bdbcdb4a753943278b759d584bb034a717b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882894"
---
# <span data-ttu-id="ab8dd-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab8dd-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ab8dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8dd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab8dd-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ab8dd-103">SYNTAX</span></span>

### <span data-ttu-id="ab8dd-104">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab8dd-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab8dd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab8dd-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab8dd-106">설명은</span><span class="sxs-lookup"><span data-stu-id="ab8dd-106">DESCRIPTION</span></span>

## <span data-ttu-id="ab8dd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab8dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8dd-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="ab8dd-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="ab8dd-109">변수</span><span class="sxs-lookup"><span data-stu-id="ab8dd-109">PARAMETERS</span></span>

### <span data-ttu-id="ab8dd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab8dd-110">-AsJob</span></span>
<span data-ttu-id="ab8dd-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ab8dd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab8dd-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="ab8dd-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="ab8dd-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8dd-114">-DefaultProfile</span></span>
<span data-ttu-id="ab8dd-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab8dd-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ab8dd-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab8dd-117">-Force</span></span>
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

### <span data-ttu-id="ab8dd-118">-계층 정책</span><span class="sxs-lookup"><span data-stu-id="ab8dd-118">-IpsecPolicies</span></span>
<span data-ttu-id="ab8dd-119">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-119">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="ab8dd-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-121">-위치</span><span class="sxs-lookup"><span data-stu-id="ab8dd-121">-Location</span></span>
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

### <span data-ttu-id="ab8dd-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ab8dd-122">-Name</span></span>
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

### <span data-ttu-id="ab8dd-123">-투-피어</span><span class="sxs-lookup"><span data-stu-id="ab8dd-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="ab8dd-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8dd-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ab8dd-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="ab8dd-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ab8dd-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-128">태그</span><span class="sxs-lookup"><span data-stu-id="ab8dd-128">-Tag</span></span>
<span data-ttu-id="ab8dd-129">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab8dd-130">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ab8dd-130">For example:</span></span>

<span data-ttu-id="ab8dd-131">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ab8dd-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ab8dd-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ab8dd-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ab8dd-133">S2S 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="ab8dd-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="ab8dd-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="ab8dd-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8dd-136">-확인</span><span class="sxs-lookup"><span data-stu-id="ab8dd-136">-Confirm</span></span>
<span data-ttu-id="ab8dd-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab8dd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8dd-138">-WhatIf</span></span>
<span data-ttu-id="ab8dd-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab8dd-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab8dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8dd-141">CommonParameters</span></span>
<span data-ttu-id="ab8dd-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8dd-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8dd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8dd-144">입력</span><span class="sxs-lookup"><span data-stu-id="ab8dd-144">INPUTS</span></span>

## <span data-ttu-id="ab8dd-145">출력</span><span class="sxs-lookup"><span data-stu-id="ab8dd-145">OUTPUTS</span></span>

### <span data-ttu-id="ab8dd-146">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ab8dd-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ab8dd-147">상속자</span><span class="sxs-lookup"><span data-stu-id="ab8dd-147">NOTES</span></span>

## <span data-ttu-id="ab8dd-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab8dd-148">RELATED LINKS</span></span>

[<span data-ttu-id="ab8dd-149">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab8dd-149">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ab8dd-150">제거-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab8dd-150">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ab8dd-151">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab8dd-151">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
