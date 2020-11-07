---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700682"
---
# <span data-ttu-id="2ccfb-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2ccfb-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="2ccfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ccfb-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccfb-103">가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="2ccfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ccfb-104">SYNTAX</span></span>

### <span data-ttu-id="2ccfb-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2ccfb-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ccfb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ccfb-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ccfb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2ccfb-107">DESCRIPTION</span></span>
<span data-ttu-id="2ccfb-108">**Add-AzVirtualNetworkSubnetConfig** cmdlet은 기존 Azure 가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="2ccfb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2ccfb-109">EXAMPLES</span></span>

### <span data-ttu-id="2ccfb-110">1: 기존 가상 네트워크에 서브넷 추가</span><span class="sxs-lookup"><span data-stu-id="2ccfb-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="2ccfb-111">이 예제에서는 먼저 만들려는 리소스의 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="2ccfb-112">그런 다음 서브넷 구성을 만들고이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="2ccfb-113">그런 다음 Add-AzVirtualNetworkSubnetConfig를 사용 하 여 가상 네트워크의 메모리 내 표현에 서브넷을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="2ccfb-114">Set-AzVirtualNetwork 명령은 새 서브넷으로 기존 가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="2ccfb-115">2: 기존 가상 네트워크에 추가 되는 서브넷에 위임 추가</span><span class="sxs-lookup"><span data-stu-id="2ccfb-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="2ccfb-116">이 예제에서는 먼저 기존 vnet을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="2ccfb-117">그런 다음 메모리에 위임 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="2ccfb-118">마지막으로, vnet에 추가 되는 위임으로 새 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="2ccfb-119">수정 된 구성은 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="2ccfb-120">변수</span><span class="sxs-lookup"><span data-stu-id="2ccfb-120">PARAMETERS</span></span>

### <span data-ttu-id="2ccfb-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2ccfb-121">-AddressPrefix</span></span>
<span data-ttu-id="2ccfb-122">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="2ccfb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccfb-123">-DefaultProfile</span></span>
<span data-ttu-id="2ccfb-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ccfb-125">-위임</span><span class="sxs-lookup"><span data-stu-id="2ccfb-125">-Delegation</span></span>
<span data-ttu-id="2ccfb-126">이 서브넷에 대 한 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="2ccfb-127">-이름</span><span class="sxs-lookup"><span data-stu-id="2ccfb-127">-Name</span></span>
<span data-ttu-id="2ccfb-128">추가할 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="2ccfb-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2ccfb-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2ccfb-130">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="2ccfb-131">이 cmdlet은이 매개 변수에서 지정 하는 개체에 가상 네트워크 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ccfb-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2ccfb-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2ccfb-133">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2ccfb-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2ccfb-134">-RouteTable</span></span>
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

### <span data-ttu-id="2ccfb-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="2ccfb-135">-RouteTableId</span></span>
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

### <span data-ttu-id="2ccfb-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ccfb-136">-ServiceEndpoint</span></span>
<span data-ttu-id="2ccfb-137">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="2ccfb-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="2ccfb-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2ccfb-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2ccfb-139">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="2ccfb-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="2ccfb-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ccfb-140">-VirtualNetwork</span></span>
<span data-ttu-id="2ccfb-141">서브넷 구성을 추가할 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="2ccfb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccfb-142">CommonParameters</span></span>
<span data-ttu-id="2ccfb-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccfb-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccfb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccfb-145">입력</span><span class="sxs-lookup"><span data-stu-id="2ccfb-145">INPUTS</span></span>

### <span data-ttu-id="2ccfb-146">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="2ccfb-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ccfb-147">System.String</span></span>

### <span data-ttu-id="2ccfb-148">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2ccfb-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="2ccfb-149">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="2ccfb-150">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2ccfb-150">System.String[]</span></span>

### <span data-ttu-id="2ccfb-151">Microsoft. \* PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="2ccfb-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="2ccfb-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="2ccfb-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="2ccfb-153">출력</span><span class="sxs-lookup"><span data-stu-id="2ccfb-153">OUTPUTS</span></span>

### <span data-ttu-id="2ccfb-154">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2ccfb-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="2ccfb-155">상속자</span><span class="sxs-lookup"><span data-stu-id="2ccfb-155">NOTES</span></span>

## <span data-ttu-id="2ccfb-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ccfb-156">RELATED LINKS</span></span>

[<span data-ttu-id="2ccfb-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2ccfb-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2ccfb-158">새로운 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2ccfb-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2ccfb-159">제거-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2ccfb-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="2ccfb-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2ccfb-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
