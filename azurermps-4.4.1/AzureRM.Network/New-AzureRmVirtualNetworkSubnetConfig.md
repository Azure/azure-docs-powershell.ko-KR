---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4211e39555f98fd21a78085f3f49749da60c2b4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527435"
---
# <span data-ttu-id="c537b-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c537b-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c537b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c537b-102">SYNOPSIS</span></span>
<span data-ttu-id="c537b-103">가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c537b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c537b-104">SYNTAX</span></span>

### <span data-ttu-id="c537b-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="c537b-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c537b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c537b-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c537b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c537b-107">DESCRIPTION</span></span>
<span data-ttu-id="c537b-108">**새 AzureRmVirtualNetworkSubnetConfig Cmdlet은** 가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="c537b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c537b-109">EXAMPLES</span></span>

### <span data-ttu-id="c537b-110">1: 서브넷 2 개와 네트워크 보안 그룹을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="c537b-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
    $networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
    New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="c537b-111">이 예제에서는 New-AzureRmVirtualSubnetConfig cmdlet을 사용 하 여 두 개의 새 서브넷 구성을 만든 다음이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="c537b-112">New-AzureRmVirtualSubnetConfig 템플릿은 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="c537b-113">이 예제에서는 frontendSubnet에 CIDR 10.0.1.0/24를 사용 하 고 RDP 액세스를 허용 하는 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="c537b-114">BackendSubnet에는 CIDR 10.0.2.0/24를 포함 하 고 동일한 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="c537b-115">변수</span><span class="sxs-lookup"><span data-stu-id="c537b-115">PARAMETERS</span></span>

### <span data-ttu-id="c537b-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c537b-116">-AddressPrefix</span></span>
<span data-ttu-id="c537b-117">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="c537b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c537b-118">-Name</span></span>
<span data-ttu-id="c537b-119">만들려는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-119">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="c537b-120">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c537b-120">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c537b-121">NetworkSecurityGroup 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-121">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="c537b-122">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c537b-122">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="c537b-123">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-123">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="c537b-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c537b-124">-RouteTable</span></span>
<span data-ttu-id="c537b-125">서브넷 구성과 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-125">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="c537b-126">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="c537b-126">-RouteTableId</span></span>
<span data-ttu-id="c537b-127">서브넷 구성과 연결 된 경로 테이블의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-127">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="c537b-128">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c537b-128">-ServiceEndpoint</span></span>
<span data-ttu-id="c537b-129">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="c537b-129">Service Endpoint Value</span></span>

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

### <span data-ttu-id="c537b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c537b-130">-DefaultProfile</span></span>
<span data-ttu-id="c537b-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c537b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c537b-132">CommonParameters</span></span>
<span data-ttu-id="c537b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c537b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c537b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c537b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c537b-135">입력</span><span class="sxs-lookup"><span data-stu-id="c537b-135">INPUTS</span></span>

## <span data-ttu-id="c537b-136">출력</span><span class="sxs-lookup"><span data-stu-id="c537b-136">OUTPUTS</span></span>

### <span data-ttu-id="c537b-137">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c537b-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c537b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c537b-138">NOTES</span></span>

## <span data-ttu-id="c537b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c537b-139">RELATED LINKS</span></span>

[<span data-ttu-id="c537b-140">추가-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c537b-140">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c537b-141">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c537b-141">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c537b-142">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c537b-142">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c537b-143">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c537b-143">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


