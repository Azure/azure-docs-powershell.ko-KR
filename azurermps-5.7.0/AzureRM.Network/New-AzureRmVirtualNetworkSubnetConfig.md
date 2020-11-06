---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: be1b0f81aa33fb0f1368e5730e80f41b9fdcabb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532107"
---
# <span data-ttu-id="890df-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="890df-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="890df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="890df-102">SYNOPSIS</span></span>
<span data-ttu-id="890df-103">가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="890df-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="890df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="890df-104">SYNTAX</span></span>

### <span data-ttu-id="890df-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="890df-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="890df-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="890df-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="890df-107">설명은</span><span class="sxs-lookup"><span data-stu-id="890df-107">DESCRIPTION</span></span>
<span data-ttu-id="890df-108">**새 AzureRmVirtualNetworkSubnetConfig Cmdlet은** 가상 네트워크 서브넷 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="890df-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="890df-109">예제의</span><span class="sxs-lookup"><span data-stu-id="890df-109">EXAMPLES</span></span>

### <span data-ttu-id="890df-110">1: 서브넷 2 개와 네트워크 보안 그룹을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="890df-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="890df-111">이 예제에서는 New-AzureRmVirtualSubnetConfig cmdlet을 사용 하 여 두 개의 새 서브넷 구성을 만든 다음이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="890df-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="890df-112">New-AzureRmVirtualSubnetConfig 템플릿은 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="890df-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="890df-113">이 예제에서는 frontendSubnet에 CIDR 10.0.1.0/24를 사용 하 고 RDP 액세스를 허용 하는 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="890df-114">BackendSubnet에는 CIDR 10.0.2.0/24를 포함 하 고 동일한 네트워크 보안 그룹을 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="890df-115">변수</span><span class="sxs-lookup"><span data-stu-id="890df-115">PARAMETERS</span></span>

### <span data-ttu-id="890df-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="890df-116">-AddressPrefix</span></span>
<span data-ttu-id="890df-117">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890df-118">-DefaultProfile</span></span>
<span data-ttu-id="890df-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="890df-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890df-120">-이름</span><span class="sxs-lookup"><span data-stu-id="890df-120">-Name</span></span>
<span data-ttu-id="890df-121">만들려는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-121">Specifies the name of the subnet configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890df-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="890df-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="890df-123">NetworkSecurityGroup 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-123">Specifies a NetworkSecurityGroup object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890df-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="890df-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="890df-125">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-125">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890df-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="890df-126">-RouteTable</span></span>
<span data-ttu-id="890df-127">서브넷 구성과 연결 된 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-127">Specifies the route table associated with the subnet configuration.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890df-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="890df-128">-RouteTableId</span></span>
<span data-ttu-id="890df-129">서브넷 구성과 연결 된 경로 테이블의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890df-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="890df-130">-ServiceEndpoint</span></span>
<span data-ttu-id="890df-131">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="890df-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="890df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890df-132">CommonParameters</span></span>
<span data-ttu-id="890df-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="890df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890df-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="890df-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890df-135">입력</span><span class="sxs-lookup"><span data-stu-id="890df-135">INPUTS</span></span>

### <span data-ttu-id="890df-136">않아야</span><span class="sxs-lookup"><span data-stu-id="890df-136">None</span></span>
<span data-ttu-id="890df-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="890df-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="890df-138">출력</span><span class="sxs-lookup"><span data-stu-id="890df-138">OUTPUTS</span></span>

### <span data-ttu-id="890df-139">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="890df-139">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="890df-140">상속자</span><span class="sxs-lookup"><span data-stu-id="890df-140">NOTES</span></span>

## <span data-ttu-id="890df-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="890df-141">RELATED LINKS</span></span>

[<span data-ttu-id="890df-142">추가-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="890df-142">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="890df-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="890df-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="890df-144">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="890df-144">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="890df-145">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="890df-145">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


