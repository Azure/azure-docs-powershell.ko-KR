---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528506"
---
# <span data-ttu-id="a34e4-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a34e4-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a34e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a34e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a34e4-103">가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a34e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a34e4-104">SYNTAX</span></span>

### <span data-ttu-id="a34e4-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a34e4-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a34e4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a34e4-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a34e4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a34e4-107">DESCRIPTION</span></span>
<span data-ttu-id="a34e4-108">**새 AzureRmVirtualNetworkSubnetConfig Cmdlet은** 가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="a34e4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a34e4-109">EXAMPLES</span></span>

### <span data-ttu-id="a34e4-110">1: 서브넷 2 개와 네트워크 보안 그룹을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="a34e4-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="a34e4-111">이 예제에서는 New-AzureRmVirtualSubnetConfig cmdlet을 사용 하 여 두 개의 새 서브넷 구성을 만든 다음이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="a34e4-112">New-AzureRmVirtualSubnetConfig 템플릿은 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="a34e4-113">이 예제에서는 frontendSubnet에 CIDR 10.0.1.0/24를 사용 하 고 RDP 액세스를 허용 하는 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="a34e4-114">BackendSubnet에는 CIDR 10.0.2.0/24를 포함 하 고 동일한 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="a34e4-115">변수</span><span class="sxs-lookup"><span data-stu-id="a34e4-115">PARAMETERS</span></span>

### <span data-ttu-id="a34e4-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a34e4-116">-AddressPrefix</span></span>
<span data-ttu-id="a34e4-117">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="a34e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a34e4-118">-DefaultProfile</span></span>
<span data-ttu-id="a34e4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a34e4-120">-위임</span><span class="sxs-lookup"><span data-stu-id="a34e4-120">-Delegation</span></span>
<span data-ttu-id="a34e4-121">이 서브넷에 대 한 작업을 수행할 수 있는 권한이 있는 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="a34e4-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a34e4-122">-Name</span></span>
<span data-ttu-id="a34e4-123">만들려는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="a34e4-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a34e4-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a34e4-125">NetworkSecurityGroup 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="a34e4-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a34e4-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a34e4-127">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a34e4-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a34e4-128">-RouteTable</span></span>
<span data-ttu-id="a34e4-129">서브넷 구성과 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a34e4-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="a34e4-130">-RouteTableId</span></span>
<span data-ttu-id="a34e4-131">서브넷 구성과 연결 된 경로 테이블의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a34e4-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a34e4-132">-ServiceEndpoint</span></span>
<span data-ttu-id="a34e4-133">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="a34e4-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="a34e4-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a34e4-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a34e4-135">서비스 끝점 정책</span><span class="sxs-lookup"><span data-stu-id="a34e4-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="a34e4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34e4-136">CommonParameters</span></span>
<span data-ttu-id="a34e4-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34e4-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34e4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34e4-139">입력</span><span class="sxs-lookup"><span data-stu-id="a34e4-139">INPUTS</span></span>

### <span data-ttu-id="a34e4-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a34e4-140">System.String</span></span>

### <span data-ttu-id="a34e4-141">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a34e4-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="a34e4-142">PSRouteTable에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a34e4-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="a34e4-143">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a34e4-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a34e4-144">System.webserver. List ' 1 [[Microsoft Azure.. 모델. PSServiceEndpointPolicy, Microsoft Azure. 명령인. 네트워크, 버전 = 6.7.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a34e4-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a34e4-145">Elegation에 ' 1 [[Microsoft.Azure.Commands.Network.Models.PSD], Microsoft Azure. 6.7.0.0, Culture = 중립, PublicKeyToken = null]] 목록이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a34e4-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a34e4-146">출력</span><span class="sxs-lookup"><span data-stu-id="a34e4-146">OUTPUTS</span></span>

### <span data-ttu-id="a34e4-147">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a34e4-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="a34e4-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a34e4-148">NOTES</span></span>

## <span data-ttu-id="a34e4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a34e4-149">RELATED LINKS</span></span>

[<span data-ttu-id="a34e4-150">추가-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a34e4-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a34e4-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a34e4-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a34e4-152">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a34e4-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a34e4-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a34e4-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


