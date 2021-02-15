---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202696"
---
# <span data-ttu-id="9cef6-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9cef6-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9cef6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cef6-102">SYNOPSIS</span></span>
<span data-ttu-id="9cef6-103">가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="9cef6-104">구문</span><span class="sxs-lookup"><span data-stu-id="9cef6-104">SYNTAX</span></span>

### <span data-ttu-id="9cef6-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="9cef6-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cef6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cef6-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cef6-107">설명</span><span class="sxs-lookup"><span data-stu-id="9cef6-107">DESCRIPTION</span></span>
<span data-ttu-id="9cef6-108">**New-AzVirtualNetworkSubnetConfig** cmdlet은 가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="9cef6-109">예제</span><span class="sxs-lookup"><span data-stu-id="9cef6-109">EXAMPLES</span></span>

### <span data-ttu-id="9cef6-110">예제 1: 두 서브넷과 네트워크 보안 그룹이 있는 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="9cef6-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="9cef6-111">이 예제에서는 New-AzVirtualSubnetConfig cmdlet을 사용하여 두 개의 새 서브넷 구성을 만든 다음 이를 사용하여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="9cef6-112">New-AzVirtualSubnetConfig 템플릿은 서브넷의 메모리 내 표현만 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="9cef6-113">이 예제에서 frontendSubnet에는 CIDR 10.0.1.0/24가 있으며 RDP 액세스를 허용하는 네트워크 보안 그룹을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="9cef6-114">backendSubnet에는 CIDR 10.0.2.0/24가 있으며 동일한 네트워크 보안 그룹을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="9cef6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cef6-115">PARAMETERS</span></span>

### <span data-ttu-id="9cef6-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9cef6-116">-AddressPrefix</span></span>
<span data-ttu-id="9cef6-117">서브넷 구성에 대한 IP 주소 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="9cef6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cef6-118">-DefaultProfile</span></span>
<span data-ttu-id="9cef6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cef6-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="9cef6-120">-Delegation</span></span>
<span data-ttu-id="9cef6-121">이 서브넷에서 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="9cef6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cef6-122">-InputObject</span></span>
<span data-ttu-id="9cef6-123">서브넷 구성과 연결된 nat 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="9cef6-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="9cef6-124">-IpAllocation</span></span>
<span data-ttu-id="9cef6-125">서브넷에 대한 IpAllocations를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="9cef6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9cef6-126">-Name</span></span>
<span data-ttu-id="9cef6-127">만들 서브넷 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="9cef6-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9cef6-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9cef6-129">NetworkSecurityGroup 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="9cef6-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9cef6-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="9cef6-131">네트워크 보안 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="9cef6-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="9cef6-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="9cef6-133">서브넷의 개인 엔드포인트에 네트워크 정책 적용을 활성화하거나 사용하지 않도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="9cef6-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="9cef6-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="9cef6-135">서브넷의 개인 링크 서비스에 네트워크 정책 적용을 활성화하거나 사용하지 않도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="9cef6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cef6-136">-ResourceId</span></span>
<span data-ttu-id="9cef6-137">서브넷 구성과 연결된 NAT 게이트웨이 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="9cef6-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9cef6-138">-RouteTable</span></span>
<span data-ttu-id="9cef6-139">서브넷 구성과 연결된 경로 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="9cef6-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="9cef6-140">-RouteTableId</span></span>
<span data-ttu-id="9cef6-141">서브넷 구성과 연결된 경로 테이블의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="9cef6-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cef6-142">-ServiceEndpoint</span></span>
<span data-ttu-id="9cef6-143">서비스 엔드포인트 값</span><span class="sxs-lookup"><span data-stu-id="9cef6-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="9cef6-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9cef6-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="9cef6-145">서비스 엔드포인트 정책</span><span class="sxs-lookup"><span data-stu-id="9cef6-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="9cef6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cef6-146">CommonParameters</span></span>
<span data-ttu-id="9cef6-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9cef6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cef6-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9cef6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cef6-149">입력</span><span class="sxs-lookup"><span data-stu-id="9cef6-149">INPUTS</span></span>

### <span data-ttu-id="9cef6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9cef6-150">System.String</span></span>

### <span data-ttu-id="9cef6-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9cef6-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="9cef6-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9cef6-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="9cef6-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="9cef6-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="9cef6-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9cef6-154">System.String[]</span></span>

### <span data-ttu-id="9cef6-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="9cef6-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="9cef6-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span><span class="sxs-lookup"><span data-stu-id="9cef6-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="9cef6-157">출력</span><span class="sxs-lookup"><span data-stu-id="9cef6-157">OUTPUTS</span></span>

### <span data-ttu-id="9cef6-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9cef6-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="9cef6-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9cef6-159">NOTES</span></span>

## <span data-ttu-id="9cef6-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cef6-160">RELATED LINKS</span></span>

[<span data-ttu-id="9cef6-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9cef6-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9cef6-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9cef6-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9cef6-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9cef6-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9cef6-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9cef6-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
