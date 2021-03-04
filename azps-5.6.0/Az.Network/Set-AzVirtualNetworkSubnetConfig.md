---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 47c56f2f55a07dc2567ca3ee2030e075d90dc324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952027"
---
# <span data-ttu-id="32871-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="32871-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="32871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32871-102">SYNOPSIS</span></span>
<span data-ttu-id="32871-103">가상 네트워크에 대한 서브넷 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="32871-104">구문</span><span class="sxs-lookup"><span data-stu-id="32871-104">SYNTAX</span></span>

### <span data-ttu-id="32871-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="32871-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32871-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="32871-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32871-107">설명</span><span class="sxs-lookup"><span data-stu-id="32871-107">DESCRIPTION</span></span>
<span data-ttu-id="32871-108">**Set-AzVirtualNetworkSubnetConfig** cmdlet은 가상 네트워크에 대한 서브넷 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="32871-109">예제</span><span class="sxs-lookup"><span data-stu-id="32871-109">EXAMPLES</span></span>

### <span data-ttu-id="32871-110">1: 서브넷의 주소 주소 수정</span><span class="sxs-lookup"><span data-stu-id="32871-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="32871-111">이 예제에서는 하나의 서브넷을 통해 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32871-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="32871-112">그런 다음 서브넷의 addressPrefix를 Set-AzVirtualNetworkSubnetConfig 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="32871-113">가상 네트워크의 메모리 내 표현에만 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32871-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="32871-114">Set-AzVirtualNetwork Azure에서 가상 네트워크를 수정하도록 호출됩니다.</span><span class="sxs-lookup"><span data-stu-id="32871-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="32871-115">2: 서브넷에 네트워크 보안 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="32871-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="32871-116">이 예제에서는 하나의 서브넷만 포함하는 하나의 가상 네트워크로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32871-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="32871-117">그런 다음 RDP 트래픽에 대한 허용 규칙이 있는 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32871-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="32871-118">Set-AzVirtualNetworkSubnetConfig cmdlet은 프런트 엔드 서브넷의 메모리 내 표현을 수정하여 새로 만든 네트워크 보안 그룹을 지적하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="32871-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="32871-119">그런 Set-AzVirtualNetwork cmdlet을 호출하여 수정된 상태를 서비스에 다시 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="32871-120">3: 서브넷에 Nat Gateway 연결</span><span class="sxs-lookup"><span data-stu-id="32871-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="32871-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="32871-121">PARAMETERS</span></span>

### <span data-ttu-id="32871-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="32871-122">-AddressPrefix</span></span>
<span data-ttu-id="32871-123">서브넷 구성에 대한 IP 주소 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32871-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32871-124">-DefaultProfile</span></span>
<span data-ttu-id="32871-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32871-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32871-126">-위임</span><span class="sxs-lookup"><span data-stu-id="32871-126">-Delegation</span></span>
<span data-ttu-id="32871-127">이 서브넷에서 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="32871-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32871-128">-InputObject</span></span>
<span data-ttu-id="32871-129">서브넷 구성과 연결된 nat 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="32871-130">-IpAllocation</span></span>
<span data-ttu-id="32871-131">서브넷에 대한 IPAllocations를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-131">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-132">-Name</span><span class="sxs-lookup"><span data-stu-id="32871-132">-Name</span></span>
<span data-ttu-id="32871-133">이 cmdlet이 구성하는 서브넷 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32871-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32871-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="32871-135">**NetworkSecurityGroup 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="32871-135">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="32871-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="32871-137">네트워크 보안 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="32871-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="32871-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="32871-139">서브넷의 개인 엔드포인트에 네트워크 정책 적용을 사용하도록 설정하거나 사용하지 않도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="32871-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="32871-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="32871-141">서브넷의 개인 링크 서비스에 네트워크 정책 적용을 사용하도록 설정하거나 사용하지 않도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="32871-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32871-142">-ResourceId</span></span>
<span data-ttu-id="32871-143">서브넷 구성과 연결된 NAT Gateway 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="32871-144">-RouteTable</span></span>
<span data-ttu-id="32871-145">네트워크 보안 그룹과 연결된 경로 테이블 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-145">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="32871-146">-RouteTableId</span></span>
<span data-ttu-id="32871-147">네트워크 보안 그룹과 연결된 경로 테이블 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="32871-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="32871-148">-ServiceEndpoint</span></span>
<span data-ttu-id="32871-149">서비스 엔드포인트 값</span><span class="sxs-lookup"><span data-stu-id="32871-149">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32871-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="32871-151">서비스 엔드포인트 정책</span><span class="sxs-lookup"><span data-stu-id="32871-151">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="32871-152">-VirtualNetwork</span></span>
<span data-ttu-id="32871-153">서브넷 구성을 포함하는 **VirtualNetwork** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32871-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32871-154">CommonParameters</span></span>
<span data-ttu-id="32871-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32871-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32871-156">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32871-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32871-157">입력</span><span class="sxs-lookup"><span data-stu-id="32871-157">INPUTS</span></span>

### <span data-ttu-id="32871-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="32871-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="32871-159">System.String</span><span class="sxs-lookup"><span data-stu-id="32871-159">System.String</span></span>

### <span data-ttu-id="32871-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32871-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="32871-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="32871-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="32871-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="32871-162">System.String[]</span></span>

### <span data-ttu-id="32871-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="32871-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="32871-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span><span class="sxs-lookup"><span data-stu-id="32871-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="32871-165">출력</span><span class="sxs-lookup"><span data-stu-id="32871-165">OUTPUTS</span></span>

### <span data-ttu-id="32871-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="32871-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="32871-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32871-167">NOTES</span></span>

## <span data-ttu-id="32871-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32871-168">RELATED LINKS</span></span>

[<span data-ttu-id="32871-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="32871-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="32871-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="32871-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="32871-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="32871-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="32871-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="32871-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
