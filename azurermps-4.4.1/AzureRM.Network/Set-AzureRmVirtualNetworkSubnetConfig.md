---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 179bfced7b73113899f525940114abb342e61f8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710976"
---
# <span data-ttu-id="27fd8-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="27fd8-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="27fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="27fd8-103">가상 네트워크의 서브넷 구성에 대 한 목표 상태를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27fd8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27fd8-104">SYNTAX</span></span>

### <span data-ttu-id="27fd8-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="27fd8-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27fd8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="27fd8-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27fd8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27fd8-107">DESCRIPTION</span></span>
<span data-ttu-id="27fd8-108">**AzureRmVirtualNetworkSubnetConfig** Cmdlet은 Azure 가상 네트워크의 서브넷 구성에 대 한 목표 상태를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="27fd8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="27fd8-109">EXAMPLES</span></span>

### <span data-ttu-id="27fd8-110">1: 서브넷의 주소 접두사 수정</span><span class="sxs-lookup"><span data-stu-id="27fd8-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="27fd8-111">이 예제에서는 서브넷이 하나인 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="27fd8-112">그런 다음 Set-AzureRmVirtualNetworkSubnetConfig 호출 하 여 서브넷의 AddressPrefix를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="27fd8-113">이는 가상 네트워크의 메모리 내 표현에만 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="27fd8-114">그런 다음 Azure에서 가상 네트워크를 수정 하기 위해 Set-AzureRmVirtualNetwork 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="27fd8-115">2: 서브넷에 네트워크 보안 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="27fd8-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="27fd8-116">이 예제에서는 하나의 서브넷만 포함 하는 하나의 가상 네트워크를 사용 하 여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="27fd8-117">그런 다음 RDP 트래픽에 허용 규칙이 있는 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="27fd8-118">Set-AzureRmVirtualNetworkSubnetConfig cmdlet은 새로 만든 네트워크 보안 그룹을 가리키도록 프런트 엔드 서브넷의 메모리 내 표현을 수정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="27fd8-119">그런 다음 수정 된 상태를 다시 서비스에 기록 하기 위해 Set-AzureRmVirtualNetwork cmdlet이 호출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="27fd8-120">변수</span><span class="sxs-lookup"><span data-stu-id="27fd8-120">PARAMETERS</span></span>

### <span data-ttu-id="27fd8-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="27fd8-121">-AddressPrefix</span></span>
<span data-ttu-id="27fd8-122">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="27fd8-123">-이름</span><span class="sxs-lookup"><span data-stu-id="27fd8-123">-Name</span></span>
<span data-ttu-id="27fd8-124">이 cmdlet이 구성 하는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-124">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="27fd8-125">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27fd8-125">-NetworkSecurityGroup</span></span>
<span data-ttu-id="27fd8-126">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-126">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="27fd8-127">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="27fd8-127">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="27fd8-128">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-128">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="27fd8-129">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="27fd8-129">-RouteTable</span></span>
<span data-ttu-id="27fd8-130">네트워크 보안 그룹과 연결 된 경로 테이블 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-130">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="27fd8-131">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="27fd8-131">-RouteTableId</span></span>
<span data-ttu-id="27fd8-132">네트워크 보안 그룹과 연결 된 경로 테이블 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-132">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="27fd8-133">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="27fd8-133">-ServiceEndpoint</span></span>
<span data-ttu-id="27fd8-134">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="27fd8-134">Service Endpoint Value</span></span>

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

### <span data-ttu-id="27fd8-135">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="27fd8-135">-VirtualNetwork</span></span>
<span data-ttu-id="27fd8-136">서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-136">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="27fd8-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fd8-137">-DefaultProfile</span></span>
<span data-ttu-id="27fd8-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27fd8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fd8-139">CommonParameters</span></span>
<span data-ttu-id="27fd8-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fd8-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27fd8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fd8-142">입력</span><span class="sxs-lookup"><span data-stu-id="27fd8-142">INPUTS</span></span>

### <span data-ttu-id="27fd8-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="27fd8-143">PSVirtualNetwork</span></span>
<span data-ttu-id="27fd8-144">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27fd8-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="27fd8-145">출력</span><span class="sxs-lookup"><span data-stu-id="27fd8-145">OUTPUTS</span></span>

### <span data-ttu-id="27fd8-146">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="27fd8-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="27fd8-147">상속자</span><span class="sxs-lookup"><span data-stu-id="27fd8-147">NOTES</span></span>

## <span data-ttu-id="27fd8-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27fd8-148">RELATED LINKS</span></span>

[<span data-ttu-id="27fd8-149">추가-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="27fd8-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="27fd8-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="27fd8-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="27fd8-151">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="27fd8-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="27fd8-152">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="27fd8-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


