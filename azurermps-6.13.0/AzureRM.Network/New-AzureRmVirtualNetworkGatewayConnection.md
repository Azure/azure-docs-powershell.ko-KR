---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: a9ad0933ce42dc0d031d9ca44d9b5ff7b84d6b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532412"
---
# <span data-ttu-id="01777-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="01777-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="01777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01777-102">SYNOPSIS</span></span>
<span data-ttu-id="01777-103">가상 네트워크 게이트웨이와 프레미스 VPN 장치 사이에 사이트 간 VPN 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01777-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01777-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01777-104">SYNTAX</span></span>

### <span data-ttu-id="01777-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="01777-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01777-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="01777-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>] [-ExpressRouteGatewayBypass]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01777-107">설명은</span><span class="sxs-lookup"><span data-stu-id="01777-107">DESCRIPTION</span></span>
<span data-ttu-id="01777-108">가상 네트워크 게이트웨이와 프레미스 VPN 장치 사이에 사이트 간 VPN 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01777-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="01777-109">예제의</span><span class="sxs-lookup"><span data-stu-id="01777-109">EXAMPLES</span></span>

### <span data-ttu-id="01777-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="01777-110">Example 1</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="01777-111">변수</span><span class="sxs-lookup"><span data-stu-id="01777-111">PARAMETERS</span></span>

### <span data-ttu-id="01777-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01777-112">-AsJob</span></span>
<span data-ttu-id="01777-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="01777-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01777-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="01777-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="01777-115">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01777-116">-DefaultProfile</span></span>
<span data-ttu-id="01777-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01777-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01777-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="01777-118">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="01777-119">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input:  True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-120">-Force</span><span class="sxs-lookup"><span data-stu-id="01777-120">-Force</span></span>

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

### <span data-ttu-id="01777-121">-계층 정책</span><span class="sxs-lookup"><span data-stu-id="01777-121">-IpsecPolicies</span></span>
<span data-ttu-id="01777-122">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="01777-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="01777-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="01777-123">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-124">-위치</span><span class="sxs-lookup"><span data-stu-id="01777-124">-Location</span></span>

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

### <span data-ttu-id="01777-125">-이름</span><span class="sxs-lookup"><span data-stu-id="01777-125">-Name</span></span>

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

### <span data-ttu-id="01777-126">-투-피어</span><span class="sxs-lookup"><span data-stu-id="01777-126">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="01777-127">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01777-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="01777-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="01777-129">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="01777-130">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-131">태그</span><span class="sxs-lookup"><span data-stu-id="01777-131">-Tag</span></span>
<span data-ttu-id="01777-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="01777-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="01777-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="01777-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="01777-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="01777-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="01777-135">S2S 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="01777-135">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01777-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="01777-136">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="01777-137">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01777-138">-확인</span><span class="sxs-lookup"><span data-stu-id="01777-138">-Confirm</span></span>
<span data-ttu-id="01777-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01777-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01777-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01777-140">-WhatIf</span></span>
<span data-ttu-id="01777-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01777-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01777-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01777-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01777-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01777-143">CommonParameters</span></span>
<span data-ttu-id="01777-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01777-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01777-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01777-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01777-146">입력</span><span class="sxs-lookup"><span data-stu-id="01777-146">INPUTS</span></span>

### <span data-ttu-id="01777-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01777-147">System.String</span></span>

### <span data-ttu-id="01777-148">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="01777-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="01777-149">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="01777-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="01777-150">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="01777-150">System.Int32</span></span>

### <span data-ttu-id="01777-151">PSPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="01777-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="01777-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="01777-152">System.Boolean</span></span>

### <span data-ttu-id="01777-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="01777-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="01777-154">System.webserver. List ' 1 [[PSIpsecPolicy, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="01777-154">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="01777-155">출력</span><span class="sxs-lookup"><span data-stu-id="01777-155">OUTPUTS</span></span>

### <span data-ttu-id="01777-156">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="01777-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="01777-157">상속자</span><span class="sxs-lookup"><span data-stu-id="01777-157">NOTES</span></span>

## <span data-ttu-id="01777-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01777-158">RELATED LINKS</span></span>

[<span data-ttu-id="01777-159">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="01777-159">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="01777-160">제거-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="01777-160">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="01777-161">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="01777-161">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
