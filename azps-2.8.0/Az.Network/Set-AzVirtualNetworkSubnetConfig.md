---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: ecaf236c04c24241cf285e3d8ca379d3bc52645a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872122"
---
# <span data-ttu-id="e43ca-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e43ca-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e43ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e43ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e43ca-103">가상 네트워크에 대 한 서브넷 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="e43ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e43ca-104">SYNTAX</span></span>

### <span data-ttu-id="e43ca-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="e43ca-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e43ca-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e43ca-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e43ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e43ca-107">DESCRIPTION</span></span>
<span data-ttu-id="e43ca-108">**AzVirtualNetworkSubnetConfig** cmdlet은 가상 네트워크에 대 한 서브넷 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="e43ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e43ca-109">EXAMPLES</span></span>

### <span data-ttu-id="e43ca-110">1: 서브넷의 주소 접두사 수정</span><span class="sxs-lookup"><span data-stu-id="e43ca-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="e43ca-111">이 예제에서는 서브넷이 하나인 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="e43ca-112">그런 다음 Set-AzVirtualNetworkSubnetConfig 호출 하 여 서브넷의 AddressPrefix를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="e43ca-113">이는 가상 네트워크의 메모리 내 표현에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e43ca-114">그런 다음 Azure에서 가상 네트워크를 수정 하기 위해 Set-AzVirtualNetwork 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="e43ca-115">2: 서브넷에 네트워크 보안 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="e43ca-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="e43ca-116">이 예제에서는 하나의 서브넷만 포함 하는 하나의 가상 네트워크를 사용 하 여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="e43ca-117">그런 다음 RDP 트래픽에 허용 규칙이 있는 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="e43ca-118">Set-AzVirtualNetworkSubnetConfig cmdlet은 새로 만든 네트워크 보안 그룹을 가리키도록 프런트 엔드 서브넷의 메모리 내 표현을 수정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="e43ca-119">그런 다음 수정 된 상태를 다시 서비스에 기록 하기 위해 Set-AzVirtualNetwork cmdlet이 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="e43ca-120">3: Nat 게이트웨이를 서브넷에 연결</span><span class="sxs-lookup"><span data-stu-id="e43ca-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="e43ca-121">변수</span><span class="sxs-lookup"><span data-stu-id="e43ca-121">PARAMETERS</span></span>

### <span data-ttu-id="e43ca-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e43ca-122">-AddressPrefix</span></span>
<span data-ttu-id="e43ca-123">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="e43ca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43ca-124">-DefaultProfile</span></span>
<span data-ttu-id="e43ca-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43ca-126">-위임</span><span class="sxs-lookup"><span data-stu-id="e43ca-126">-Delegation</span></span>
<span data-ttu-id="e43ca-127">이 서브넷에 대 한 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="e43ca-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e43ca-128">-InputObject</span></span>
<span data-ttu-id="e43ca-129">서브넷 구성과 연결 된 nat 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e43ca-130">-이름</span><span class="sxs-lookup"><span data-stu-id="e43ca-130">-Name</span></span>
<span data-ttu-id="e43ca-131">이 cmdlet이 구성 하는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="e43ca-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e43ca-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e43ca-133">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-133">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="e43ca-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e43ca-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e43ca-135">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e43ca-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e43ca-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="e43ca-137">서브넷의 개인 끝점에 대 한 네트워크 정책 적용을 사용 하거나 사용 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="e43ca-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="e43ca-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="e43ca-139">서브넷의 개인 링크 서비스에 대 한 네트워크 정책 적용을 사용 하거나 사용 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="e43ca-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43ca-140">-ResourceId</span></span>
<span data-ttu-id="e43ca-141">서브넷 구성과 연결 된 NAT 게이트웨이 리소스의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e43ca-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e43ca-142">-RouteTable</span></span>
<span data-ttu-id="e43ca-143">네트워크 보안 그룹과 연결 된 경로 테이블 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-143">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="e43ca-144">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e43ca-144">-RouteTableId</span></span>
<span data-ttu-id="e43ca-145">네트워크 보안 그룹과 연결 된 경로 테이블 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="e43ca-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e43ca-146">-ServiceEndpoint</span></span>
<span data-ttu-id="e43ca-147">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="e43ca-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e43ca-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e43ca-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e43ca-149">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="e43ca-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="e43ca-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e43ca-150">-VirtualNetwork</span></span>
<span data-ttu-id="e43ca-151">서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="e43ca-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43ca-152">CommonParameters</span></span>
<span data-ttu-id="e43ca-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e43ca-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43ca-154">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e43ca-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43ca-155">입력</span><span class="sxs-lookup"><span data-stu-id="e43ca-155">INPUTS</span></span>

### <span data-ttu-id="e43ca-156">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e43ca-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="e43ca-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e43ca-157">System.String</span></span>

### <span data-ttu-id="e43ca-158">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e43ca-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e43ca-159">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e43ca-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e43ca-160">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e43ca-160">System.String[]</span></span>

### <span data-ttu-id="e43ca-161">Microsoft. \* PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="e43ca-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="e43ca-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="e43ca-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="e43ca-163">출력</span><span class="sxs-lookup"><span data-stu-id="e43ca-163">OUTPUTS</span></span>

### <span data-ttu-id="e43ca-164">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e43ca-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e43ca-165">상속자</span><span class="sxs-lookup"><span data-stu-id="e43ca-165">NOTES</span></span>

## <span data-ttu-id="e43ca-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e43ca-166">RELATED LINKS</span></span>

[<span data-ttu-id="e43ca-167">추가-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e43ca-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e43ca-168">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e43ca-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e43ca-169">새로운 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e43ca-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e43ca-170">제거-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e43ca-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
