---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1129b24c69dc362ea4d700be28a0823afa860885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711065"
---
# <span data-ttu-id="0daf8-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0daf8-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="0daf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0daf8-102">SYNOPSIS</span></span>
<span data-ttu-id="0daf8-103">가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0daf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0daf8-104">SYNTAX</span></span>

### <span data-ttu-id="0daf8-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="0daf8-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0daf8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0daf8-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0daf8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0daf8-107">DESCRIPTION</span></span>
<span data-ttu-id="0daf8-108">**Add-AzureRmVirtualNetworkSubnetConfig** cmdlet은 기존 Azure 가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="0daf8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0daf8-109">EXAMPLES</span></span>

### <span data-ttu-id="0daf8-110">1: 기존 가상 네트워크에 서브넷 추가</span><span class="sxs-lookup"><span data-stu-id="0daf8-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="0daf8-111">이 예제에서는 먼저 만들려는 리소스의 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="0daf8-112">그런 다음 서브넷 구성을 만들고이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="0daf8-113">그런 다음 Add-AzureRmVirtualNetworkSubnetConfig를 사용 하 여 가상 네트워크의 메모리 내 표현에 서브넷을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="0daf8-114">Set-AzureRmVirtualNetwork 명령은 새 서브넷으로 기존 가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="0daf8-115">2: 기존 가상 네트워크에 추가 되는 서브넷에 위임 추가</span><span class="sxs-lookup"><span data-stu-id="0daf8-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="0daf8-116">이 예제에서는 먼저 기존 vnet을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="0daf8-117">그런 다음 메모리에 위임 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="0daf8-118">마지막으로, vnet에 추가 되는 위임으로 새 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="0daf8-119">수정 된 구성은 서버로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="0daf8-120">변수</span><span class="sxs-lookup"><span data-stu-id="0daf8-120">PARAMETERS</span></span>

### <span data-ttu-id="0daf8-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0daf8-121">-AddressPrefix</span></span>
<span data-ttu-id="0daf8-122">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0daf8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daf8-123">-DefaultProfile</span></span>
<span data-ttu-id="0daf8-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0daf8-125">-위임</span><span class="sxs-lookup"><span data-stu-id="0daf8-125">-Delegation</span></span>
<span data-ttu-id="0daf8-126">이 서브넷에 대 한 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0daf8-127">-이름</span><span class="sxs-lookup"><span data-stu-id="0daf8-127">-Name</span></span>
<span data-ttu-id="0daf8-128">추가할 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="0daf8-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0daf8-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0daf8-130">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="0daf8-131">이 cmdlet은이 매개 변수에서 지정 하는 개체에 가상 네트워크 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="0daf8-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0daf8-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="0daf8-133">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="0daf8-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0daf8-134">-RouteTable</span></span>
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

### <span data-ttu-id="0daf8-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="0daf8-135">-RouteTableId</span></span>
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

### <span data-ttu-id="0daf8-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0daf8-136">-ServiceEndpoint</span></span>
<span data-ttu-id="0daf8-137">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="0daf8-137">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0daf8-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0daf8-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="0daf8-139">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="0daf8-139">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0daf8-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0daf8-140">-VirtualNetwork</span></span>
<span data-ttu-id="0daf8-141">서브넷 구성을 추가할 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="0daf8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daf8-142">CommonParameters</span></span>
<span data-ttu-id="0daf8-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daf8-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0daf8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daf8-145">입력</span><span class="sxs-lookup"><span data-stu-id="0daf8-145">INPUTS</span></span>

### <span data-ttu-id="0daf8-146">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0daf8-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="0daf8-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0daf8-147">System.String</span></span>

### <span data-ttu-id="0daf8-148">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0daf8-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="0daf8-149">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0daf8-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="0daf8-150">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0daf8-150">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0daf8-151">System.webserver. List ' 1 [[Microsoft Azure.. 모델. PSServiceEndpointPolicy, Microsoft Azure. 명령인. 네트워크, 버전 = 6.7.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0daf8-151">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0daf8-152">Elegation에 ' 1 [[Microsoft.Azure.Commands.Network.Models.PSD], Microsoft Azure. 6.7.0.0, Culture = 중립, PublicKeyToken = null]] 목록이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0daf8-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0daf8-153">출력</span><span class="sxs-lookup"><span data-stu-id="0daf8-153">OUTPUTS</span></span>

### <span data-ttu-id="0daf8-154">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0daf8-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0daf8-155">상속자</span><span class="sxs-lookup"><span data-stu-id="0daf8-155">NOTES</span></span>

## <span data-ttu-id="0daf8-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0daf8-156">RELATED LINKS</span></span>

[<span data-ttu-id="0daf8-157">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0daf8-157">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0daf8-158">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0daf8-158">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0daf8-159">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0daf8-159">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0daf8-160">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0daf8-160">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


