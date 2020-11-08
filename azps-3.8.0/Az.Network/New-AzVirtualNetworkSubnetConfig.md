---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 144d04172f3169075a32c5e8111a90ff407532b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043229"
---
# <span data-ttu-id="20f80-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20f80-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="20f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f80-102">SYNOPSIS</span></span>
<span data-ttu-id="20f80-103">가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="20f80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20f80-104">SYNTAX</span></span>

### <span data-ttu-id="20f80-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="20f80-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20f80-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="20f80-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f80-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20f80-107">DESCRIPTION</span></span>
<span data-ttu-id="20f80-108">**새 AzVirtualNetworkSubnetConfig Cmdlet은** 가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="20f80-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20f80-109">EXAMPLES</span></span>

### <span data-ttu-id="20f80-110">1: 서브넷 2 개와 네트워크 보안 그룹을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="20f80-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
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

<span data-ttu-id="20f80-111">이 예제에서는 New-AzVirtualSubnetConfig cmdlet을 사용 하 여 두 개의 새 서브넷 구성을 만든 다음이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="20f80-112">New-AzVirtualSubnetConfig 템플릿은 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="20f80-113">이 예제에서는 frontendSubnet에 CIDR 10.0.1.0/24를 사용 하 고 RDP 액세스를 허용 하는 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="20f80-114">BackendSubnet에는 CIDR 10.0.2.0/24를 포함 하 고 동일한 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="20f80-115">변수</span><span class="sxs-lookup"><span data-stu-id="20f80-115">PARAMETERS</span></span>

### <span data-ttu-id="20f80-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="20f80-116">-AddressPrefix</span></span>
<span data-ttu-id="20f80-117">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="20f80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f80-118">-DefaultProfile</span></span>
<span data-ttu-id="20f80-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f80-120">-위임</span><span class="sxs-lookup"><span data-stu-id="20f80-120">-Delegation</span></span>
<span data-ttu-id="20f80-121">이 서브넷에 대 한 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="20f80-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20f80-122">-InputObject</span></span>
<span data-ttu-id="20f80-123">서브넷 구성과 연결 된 nat 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="20f80-124">-이름</span><span class="sxs-lookup"><span data-stu-id="20f80-124">-Name</span></span>
<span data-ttu-id="20f80-125">만들려는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="20f80-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20f80-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="20f80-127">NetworkSecurityGroup 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="20f80-128">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="20f80-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="20f80-129">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="20f80-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="20f80-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="20f80-131">서브넷의 개인 끝점에 대 한 네트워크 정책 적용을 사용 하거나 사용 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="20f80-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="20f80-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="20f80-133">서브넷의 개인 링크 서비스에 대 한 네트워크 정책 적용을 사용 하거나 사용 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="20f80-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20f80-134">-ResourceId</span></span>
<span data-ttu-id="20f80-135">서브넷 구성과 연결 된 NAT 게이트웨이 리소스의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="20f80-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="20f80-136">-RouteTable</span></span>
<span data-ttu-id="20f80-137">서브넷 구성과 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="20f80-138">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="20f80-138">-RouteTableId</span></span>
<span data-ttu-id="20f80-139">서브넷 구성과 연결 된 경로 테이블의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="20f80-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="20f80-140">-ServiceEndpoint</span></span>
<span data-ttu-id="20f80-141">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="20f80-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="20f80-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="20f80-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="20f80-143">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="20f80-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="20f80-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f80-144">CommonParameters</span></span>
<span data-ttu-id="20f80-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20f80-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f80-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20f80-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f80-147">입력</span><span class="sxs-lookup"><span data-stu-id="20f80-147">INPUTS</span></span>

### <span data-ttu-id="20f80-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="20f80-148">System.String</span></span>

### <span data-ttu-id="20f80-149">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20f80-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="20f80-150">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="20f80-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="20f80-151">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="20f80-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="20f80-152">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="20f80-152">System.String[]</span></span>

### <span data-ttu-id="20f80-153">Microsoft. \* PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="20f80-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="20f80-154">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="20f80-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="20f80-155">출력</span><span class="sxs-lookup"><span data-stu-id="20f80-155">OUTPUTS</span></span>

### <span data-ttu-id="20f80-156">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="20f80-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="20f80-157">상속자</span><span class="sxs-lookup"><span data-stu-id="20f80-157">NOTES</span></span>

## <span data-ttu-id="20f80-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20f80-158">RELATED LINKS</span></span>

[<span data-ttu-id="20f80-159">추가-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20f80-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20f80-160">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20f80-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20f80-161">제거-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20f80-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20f80-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20f80-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
