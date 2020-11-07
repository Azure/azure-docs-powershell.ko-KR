---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fea7f3f3d24595cdddd9635e73e3073efe5cb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870821"
---
# <span data-ttu-id="5b153-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b153-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5b153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b153-102">SYNOPSIS</span></span>
<span data-ttu-id="5b153-103">가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="5b153-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b153-104">SYNTAX</span></span>

### <span data-ttu-id="5b153-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="5b153-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b153-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b153-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b153-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5b153-107">DESCRIPTION</span></span>
<span data-ttu-id="5b153-108">**Add-AzVirtualNetworkSubnetConfig** cmdlet은 기존 Azure 가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="5b153-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5b153-109">EXAMPLES</span></span>

### <span data-ttu-id="5b153-110">1: 기존 가상 네트워크에 서브넷 추가</span><span class="sxs-lookup"><span data-stu-id="5b153-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="5b153-111">이 예제에서는 먼저 만들려는 리소스의 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="5b153-112">그런 다음 서브넷 구성을 만들고이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="5b153-113">그런 다음 Add-AzVirtualNetworkSubnetConfig를 사용 하 여 가상 네트워크의 메모리 내 표현에 서브넷을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5b153-114">Set-AzVirtualNetwork 명령은 새 서브넷으로 기존 가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="5b153-115">2: 기존 가상 네트워크에 추가 되는 서브넷에 위임 추가</span><span class="sxs-lookup"><span data-stu-id="5b153-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="5b153-116">이 예제에서는 먼저 기존 vnet을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="5b153-117">그런 다음 메모리에 위임 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="5b153-118">마지막으로, vnet에 추가 되는 위임으로 새 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="5b153-119">수정 된 구성은 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="5b153-120">변수</span><span class="sxs-lookup"><span data-stu-id="5b153-120">PARAMETERS</span></span>

### <span data-ttu-id="5b153-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5b153-121">-AddressPrefix</span></span>
<span data-ttu-id="5b153-122">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="5b153-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b153-123">-DefaultProfile</span></span>
<span data-ttu-id="5b153-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b153-125">-위임</span><span class="sxs-lookup"><span data-stu-id="5b153-125">-Delegation</span></span>
<span data-ttu-id="5b153-126">이 서브넷에 대 한 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="5b153-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b153-127">-InputObject</span></span>
<span data-ttu-id="5b153-128">서브넷 구성과 연결 된 nat 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="5b153-129">-이름</span><span class="sxs-lookup"><span data-stu-id="5b153-129">-Name</span></span>
<span data-ttu-id="5b153-130">추가할 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-130">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="5b153-131">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b153-131">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5b153-132">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-132">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="5b153-133">이 cmdlet은이 매개 변수에서 지정 하는 개체에 가상 네트워크 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-133">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b153-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5b153-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5b153-135">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="5b153-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5b153-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="5b153-137">서브넷의 개인 끝점에 대 한 네트워크 정책 적용을 사용 하거나 사용 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="5b153-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5b153-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="5b153-139">서브넷의 개인 링크 서비스에 대 한 네트워크 정책 적용을 사용 하거나 사용 하지 않도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="5b153-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b153-140">-ResourceId</span></span>
<span data-ttu-id="5b153-141">서브넷 구성과 연결 된 NAT 게이트웨이 리소스의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="5b153-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5b153-142">-RouteTable</span></span>
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

### <span data-ttu-id="5b153-143">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="5b153-143">-RouteTableId</span></span>
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

### <span data-ttu-id="5b153-144">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b153-144">-ServiceEndpoint</span></span>
<span data-ttu-id="5b153-145">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="5b153-145">Service Endpoint Value</span></span>

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

### <span data-ttu-id="5b153-146">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5b153-146">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5b153-147">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="5b153-147">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="5b153-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b153-148">-VirtualNetwork</span></span>
<span data-ttu-id="5b153-149">서브넷 구성을 추가할 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-149">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="5b153-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b153-150">CommonParameters</span></span>
<span data-ttu-id="5b153-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b153-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b153-152">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b153-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b153-153">입력</span><span class="sxs-lookup"><span data-stu-id="5b153-153">INPUTS</span></span>

### <span data-ttu-id="5b153-154">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5b153-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5b153-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b153-155">System.String</span></span>

### <span data-ttu-id="5b153-156">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5b153-156">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="5b153-157">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5b153-157">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="5b153-158">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5b153-158">System.String[]</span></span>

### <span data-ttu-id="5b153-159">Microsoft. \* PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="5b153-159">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="5b153-160">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="5b153-160">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="5b153-161">출력</span><span class="sxs-lookup"><span data-stu-id="5b153-161">OUTPUTS</span></span>

### <span data-ttu-id="5b153-162">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5b153-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5b153-163">상속자</span><span class="sxs-lookup"><span data-stu-id="5b153-163">NOTES</span></span>

## <span data-ttu-id="5b153-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b153-164">RELATED LINKS</span></span>

[<span data-ttu-id="5b153-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b153-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5b153-166">새로운 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b153-166">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5b153-167">제거-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b153-167">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5b153-168">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b153-168">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
