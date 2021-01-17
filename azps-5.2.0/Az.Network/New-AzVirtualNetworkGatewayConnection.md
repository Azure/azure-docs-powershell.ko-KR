---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323476"
---
# <span data-ttu-id="ed92c-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed92c-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ed92c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed92c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed92c-103">가상 네트워크 게이트웨이와 프레미스 VPN 디바이스 간에 사이트 간 VPN 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="ed92c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed92c-104">SYNTAX</span></span>

### <span data-ttu-id="ed92c-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="ed92c-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed92c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed92c-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed92c-107">설명</span><span class="sxs-lookup"><span data-stu-id="ed92c-107">DESCRIPTION</span></span>
<span data-ttu-id="ed92c-108">가상 네트워크 게이트웨이와 프레미스 VPN 디바이스 간에 사이트 간 VPN 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="ed92c-109">예제</span><span class="sxs-lookup"><span data-stu-id="ed92c-109">EXAMPLES</span></span>

### <span data-ttu-id="ed92c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed92c-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="ed92c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed92c-111">PARAMETERS</span></span>

### <span data-ttu-id="ed92c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed92c-112">-AsJob</span></span>
<span data-ttu-id="ed92c-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ed92c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed92c-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="ed92c-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="ed92c-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="ed92c-115">-ConnectionProtocol</span></span>
<span data-ttu-id="ed92c-116">게이트웨이 연결 프로토콜:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="ed92c-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed92c-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="ed92c-117">-ConnectionType</span></span>

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

### <span data-ttu-id="ed92c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed92c-118">-DefaultProfile</span></span>
<span data-ttu-id="ed92c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed92c-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ed92c-120">-EnableBgp</span></span>

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

### <span data-ttu-id="ed92c-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="ed92c-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed92c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ed92c-122">-Force</span></span>

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

### <span data-ttu-id="ed92c-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="ed92c-123">-IpsecPolicies</span></span>
<span data-ttu-id="ed92c-124">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed92c-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="ed92c-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="ed92c-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ed92c-126">-Location</span></span>

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

### <span data-ttu-id="ed92c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ed92c-127">-Name</span></span>

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

### <span data-ttu-id="ed92c-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="ed92c-128">-Peer</span></span>

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

### <span data-ttu-id="ed92c-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="ed92c-129">-PeerId</span></span>

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

### <span data-ttu-id="ed92c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed92c-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="ed92c-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="ed92c-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="ed92c-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="ed92c-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="ed92c-133">연결의 데드 피어 검색 시간 제한(초)</span><span class="sxs-lookup"><span data-stu-id="ed92c-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="ed92c-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="ed92c-134">-SharedKey</span></span>

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

### <span data-ttu-id="ed92c-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed92c-135">-Tag</span></span>
<span data-ttu-id="ed92c-136">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed92c-137">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ed92c-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ed92c-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ed92c-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="ed92c-139">트래픽 선택기 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-139">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed92c-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed92c-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="ed92c-141">이 S2S VPN 터널에 PrivateIP를 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="ed92c-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed92c-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ed92c-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ed92c-143">S2S 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="ed92c-143">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="ed92c-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="ed92c-144">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="ed92c-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="ed92c-145">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="ed92c-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed92c-146">-Confirm</span></span>
<span data-ttu-id="ed92c-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed92c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed92c-148">-WhatIf</span></span>
<span data-ttu-id="ed92c-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ed92c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed92c-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed92c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed92c-151">CommonParameters</span></span>
<span data-ttu-id="ed92c-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed92c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed92c-153">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ed92c-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed92c-154">입력</span><span class="sxs-lookup"><span data-stu-id="ed92c-154">INPUTS</span></span>

### <span data-ttu-id="ed92c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ed92c-155">System.String</span></span>

### <span data-ttu-id="ed92c-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed92c-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ed92c-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed92c-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="ed92c-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ed92c-158">System.Int32</span></span>

### <span data-ttu-id="ed92c-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="ed92c-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="ed92c-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed92c-160">System.Boolean</span></span>

### <span data-ttu-id="ed92c-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ed92c-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ed92c-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="ed92c-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="ed92c-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="ed92c-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="ed92c-164">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed92c-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed92c-165">출력</span><span class="sxs-lookup"><span data-stu-id="ed92c-165">OUTPUTS</span></span>

### <span data-ttu-id="ed92c-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed92c-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ed92c-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed92c-167">NOTES</span></span>

## <span data-ttu-id="ed92c-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed92c-168">RELATED LINKS</span></span>

[<span data-ttu-id="ed92c-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed92c-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ed92c-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed92c-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ed92c-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ed92c-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
