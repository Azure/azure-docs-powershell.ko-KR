---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 120e20eb62b5475a587a3d272e84c7af1e40cd45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202716"
---
# <span data-ttu-id="6bcb0-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6bcb0-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6bcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcb0-103">가상 네트워크 게이트웨이와 프레미스 VPN 디바이스 간에 사이트 간 VPN 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="6bcb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="6bcb0-104">SYNTAX</span></span>

### <span data-ttu-id="6bcb0-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="6bcb0-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bcb0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcb0-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bcb0-107">설명</span><span class="sxs-lookup"><span data-stu-id="6bcb0-107">DESCRIPTION</span></span>
<span data-ttu-id="6bcb0-108">가상 네트워크 게이트웨이와 프레미스 VPN 디바이스 간에 사이트 간 VPN 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="6bcb0-109">예제</span><span class="sxs-lookup"><span data-stu-id="6bcb0-109">EXAMPLES</span></span>

### <span data-ttu-id="6bcb0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6bcb0-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="6bcb0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bcb0-111">PARAMETERS</span></span>

### <span data-ttu-id="6bcb0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bcb0-112">-AsJob</span></span>
<span data-ttu-id="6bcb0-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6bcb0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bcb0-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="6bcb0-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="6bcb0-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="6bcb0-115">-ConnectionProtocol</span></span>
<span data-ttu-id="6bcb0-116">게이트웨이 연결 프로토콜:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="6bcb0-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="6bcb0-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="6bcb0-117">-ConnectionType</span></span>

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

### <span data-ttu-id="6bcb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcb0-118">-DefaultProfile</span></span>
<span data-ttu-id="6bcb0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bcb0-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6bcb0-120">-EnableBgp</span></span>

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

### <span data-ttu-id="6bcb0-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="6bcb0-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="6bcb0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6bcb0-122">-Force</span></span>

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

### <span data-ttu-id="6bcb0-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="6bcb0-123">-IpsecPolicies</span></span>
<span data-ttu-id="6bcb0-124">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="6bcb0-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6bcb0-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="6bcb0-126">-Location</span><span class="sxs-lookup"><span data-stu-id="6bcb0-126">-Location</span></span>

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

### <span data-ttu-id="6bcb0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6bcb0-127">-Name</span></span>

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

### <span data-ttu-id="6bcb0-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="6bcb0-128">-Peer</span></span>

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

### <span data-ttu-id="6bcb0-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="6bcb0-129">-PeerId</span></span>

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

### <span data-ttu-id="6bcb0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bcb0-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="6bcb0-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="6bcb0-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="6bcb0-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6bcb0-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="6bcb0-133">연결의 데드 피어 검색 시간 제한(초)</span><span class="sxs-lookup"><span data-stu-id="6bcb0-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="6bcb0-134">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="6bcb0-134">-ConnectionMode</span></span>
<span data-ttu-id="6bcb0-135">Virtual Network 게이트웨이 연결 모드</span><span class="sxs-lookup"><span data-stu-id="6bcb0-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb0-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="6bcb0-136">-SharedKey</span></span>

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

### <span data-ttu-id="6bcb0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6bcb0-137">-Tag</span></span>
<span data-ttu-id="6bcb0-138">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6bcb0-139">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6bcb0-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6bcb0-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6bcb0-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="6bcb0-141">트래픽 선택기 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-141">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="6bcb0-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="6bcb0-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="6bcb0-143">이 S2S VPN 터널에 PrivateIP를 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="6bcb0-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="6bcb0-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6bcb0-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6bcb0-145">S2S 연결에 정책 기반 트래픽 선택기 사용</span><span class="sxs-lookup"><span data-stu-id="6bcb0-145">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="6bcb0-146">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="6bcb0-146">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="6bcb0-147">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="6bcb0-147">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="6bcb0-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bcb0-148">-Confirm</span></span>
<span data-ttu-id="6bcb0-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bcb0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bcb0-150">-WhatIf</span></span>
<span data-ttu-id="6bcb0-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6bcb0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bcb0-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bcb0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcb0-153">CommonParameters</span></span>
<span data-ttu-id="6bcb0-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcb0-155">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6bcb0-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcb0-156">입력</span><span class="sxs-lookup"><span data-stu-id="6bcb0-156">INPUTS</span></span>

### <span data-ttu-id="6bcb0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="6bcb0-157">System.String</span></span>

### <span data-ttu-id="6bcb0-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6bcb0-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="6bcb0-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6bcb0-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="6bcb0-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6bcb0-160">System.Int32</span></span>

### <span data-ttu-id="6bcb0-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6bcb0-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="6bcb0-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bcb0-162">System.Boolean</span></span>

### <span data-ttu-id="6bcb0-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6bcb0-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6bcb0-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="6bcb0-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="6bcb0-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="6bcb0-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="6bcb0-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bcb0-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bcb0-167">출력</span><span class="sxs-lookup"><span data-stu-id="6bcb0-167">OUTPUTS</span></span>

### <span data-ttu-id="6bcb0-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6bcb0-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6bcb0-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6bcb0-169">NOTES</span></span>

## <span data-ttu-id="6bcb0-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bcb0-170">RELATED LINKS</span></span>

[<span data-ttu-id="6bcb0-171">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6bcb0-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6bcb0-172">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6bcb0-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6bcb0-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6bcb0-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
