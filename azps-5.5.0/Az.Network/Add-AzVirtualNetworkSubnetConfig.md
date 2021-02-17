---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207024"
---
# <span data-ttu-id="b66ce-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b66ce-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b66ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b66ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b66ce-103">가상 네트워크에 서브넷 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="b66ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="b66ce-104">SYNTAX</span></span>

### <span data-ttu-id="b66ce-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="b66ce-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b66ce-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b66ce-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b66ce-107">설명</span><span class="sxs-lookup"><span data-stu-id="b66ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b66ce-108">**Add-AzVirtualNetworkSubnetConfig** cmdlet은 기존 Azure 가상 네트워크에 서브넷 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="b66ce-109">예제</span><span class="sxs-lookup"><span data-stu-id="b66ce-109">EXAMPLES</span></span>

### <span data-ttu-id="b66ce-110">예제 1: 기존 가상 네트워크에 서브넷 추가</span><span class="sxs-lookup"><span data-stu-id="b66ce-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="b66ce-111">이 예제에서는 먼저 만들 리소스의 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="b66ce-112">그런 다음 서브넷 구성을 만들고 이를 사용하여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="b66ce-113">그런 Add-AzVirtualNetworkSubnetConfig 가상 네트워크의 메모리 내 표현에 서브넷을 추가하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b66ce-114">이 Set-AzVirtualNetwork 새 서브넷으로 기존 가상 네트워크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="b66ce-115">예제 2: 기존 가상 네트워크에 추가되는 서브넷에 위임 추가</span><span class="sxs-lookup"><span data-stu-id="b66ce-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="b66ce-116">이 예제에서는 먼저 기존 vnet을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="b66ce-117">그런 다음 메모리에 위임 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="b66ce-118">마지막으로 vnet에 추가된 위임이 있는 새 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="b66ce-119">그러면 수정된 구성이 서버로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="b66ce-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b66ce-120">PARAMETERS</span></span>

### <span data-ttu-id="b66ce-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b66ce-121">-AddressPrefix</span></span>
<span data-ttu-id="b66ce-122">서브넷 구성에 대한 IP 주소 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="b66ce-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66ce-123">-DefaultProfile</span></span>
<span data-ttu-id="b66ce-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b66ce-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="b66ce-125">-Delegation</span></span>
<span data-ttu-id="b66ce-126">이 서브넷에서 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="b66ce-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b66ce-127">-InputObject</span></span>
<span data-ttu-id="b66ce-128">서브넷 구성과 연결된 nat 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b66ce-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b66ce-129">-IpAllocation</span></span>
<span data-ttu-id="b66ce-130">서브넷에 대한 IpAllocations를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="b66ce-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b66ce-131">-Name</span></span>
<span data-ttu-id="b66ce-132">추가할 서브넷 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="b66ce-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b66ce-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b66ce-134">**NetworkSecurityGroup 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="b66ce-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b66ce-135">이 cmdlet은 이 매개 변수가 지정하는 개체에 가상 네트워크 서브넷 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b66ce-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b66ce-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b66ce-137">네트워크 보안 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="b66ce-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="b66ce-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="b66ce-139">서브넷의 개인 엔드포인트에 네트워크 정책 적용을 활성화하거나 사용하지 않도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="b66ce-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="b66ce-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="b66ce-141">서브넷의 개인 링크 서비스에 네트워크 정책 적용을 활성화하거나 사용하지 않도록 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="b66ce-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b66ce-142">-ResourceId</span></span>
<span data-ttu-id="b66ce-143">서브넷 구성과 연결된 NAT 게이트웨이 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="b66ce-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b66ce-144">-RouteTable</span></span>
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

### <span data-ttu-id="b66ce-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="b66ce-145">-RouteTableId</span></span>
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

### <span data-ttu-id="b66ce-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b66ce-146">-ServiceEndpoint</span></span>
<span data-ttu-id="b66ce-147">서비스 엔드포인트 값</span><span class="sxs-lookup"><span data-stu-id="b66ce-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="b66ce-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b66ce-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b66ce-149">서비스 엔드포인트 정책</span><span class="sxs-lookup"><span data-stu-id="b66ce-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="b66ce-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b66ce-150">-VirtualNetwork</span></span>
<span data-ttu-id="b66ce-151">서브넷 구성을 추가할 **VirtualNetwork** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="b66ce-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66ce-152">CommonParameters</span></span>
<span data-ttu-id="b66ce-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b66ce-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66ce-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b66ce-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66ce-155">입력</span><span class="sxs-lookup"><span data-stu-id="b66ce-155">INPUTS</span></span>

### <span data-ttu-id="b66ce-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b66ce-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b66ce-157">System.String</span><span class="sxs-lookup"><span data-stu-id="b66ce-157">System.String</span></span>

### <span data-ttu-id="b66ce-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b66ce-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="b66ce-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b66ce-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="b66ce-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b66ce-160">System.String[]</span></span>

### <span data-ttu-id="b66ce-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="b66ce-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="b66ce-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span><span class="sxs-lookup"><span data-stu-id="b66ce-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="b66ce-163">출력</span><span class="sxs-lookup"><span data-stu-id="b66ce-163">OUTPUTS</span></span>

### <span data-ttu-id="b66ce-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b66ce-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b66ce-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b66ce-165">NOTES</span></span>

## <span data-ttu-id="b66ce-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b66ce-166">RELATED LINKS</span></span>

[<span data-ttu-id="b66ce-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b66ce-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b66ce-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b66ce-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b66ce-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b66ce-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b66ce-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b66ce-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
