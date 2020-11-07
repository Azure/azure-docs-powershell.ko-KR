---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: a81f8b260b0631692bb24a571bcb86b8ecf038d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882602"
---
# <span data-ttu-id="276f8-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="276f8-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="276f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="276f8-102">SYNOPSIS</span></span>
<span data-ttu-id="276f8-103">가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="276f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="276f8-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="276f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="276f8-105">DESCRIPTION</span></span>
<span data-ttu-id="276f8-106">**새 AzureRmVirtualNetwork** Cmdlet은 Azure 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="276f8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="276f8-107">EXAMPLES</span></span>

### <span data-ttu-id="276f8-108">1: 서브넷 두 개를 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="276f8-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="276f8-109">이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="276f8-110">먼저 새 리소스 그룹이 centralus 지역에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="276f8-111">그런 다음이 예제는 두 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="276f8-112">New-AzureRmVirtualNetworkSubnetConfig cmdlet은 서버 쪽에 서브넷을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="276f8-113">FrontendSubnet 라는 서브넷과 backendSubnet 라는 서브넷 하나가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="276f8-114">그런 다음 New-AzureRmVirtualNetwork cmdlet은 CIDR 10.0.0.0/16을 주소 접두사와 두 개의 서브넷으로 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="276f8-115">2: DNS 설정을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="276f8-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="276f8-116">이 예제에서는 서브넷 2 개와 DNS 서버 두 개를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="276f8-117">가상 네트워크에서 DNS 서버를 지정 하는 효과는이 가상 네트워크에 배포 된 Nic/Vm이이 DNS 서버를 기본값으로 상속 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="276f8-118">이러한 기본값은 nic 수준 설정을 통해 NIC 별로 덮어쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="276f8-119">VNET에 dns 서버가 지정 되지 않고 Nic에 DNS 서버가 없으면 기본 Azure DNS 서버가 DNS 확인에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="276f8-120">3: 네트워크 보안 그룹을 참조 하는 서브넷을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="276f8-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="276f8-121">이 예제에서는 네트워크 보안 그룹을 참조 하는 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="276f8-122">먼저,이 예제에서는 만들려는 리소스에 대 한 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="276f8-123">그런 다음 인바운드 RDP 액세스를 허용 하는 네트워크 보안 그룹을 만들지만, 그렇지 않은 경우에는 기본 네트워크 보안 그룹 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="276f8-124">그런 다음 New-AzureRmVirtualNetworkSubnetConfig cmdlet은 생성 된 네트워크 보안 그룹을 둘 다 참조 하는 두 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="276f8-125">그런 다음 New-AzureRmVirtualNetwork 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="276f8-126">변수</span><span class="sxs-lookup"><span data-stu-id="276f8-126">PARAMETERS</span></span>

### <span data-ttu-id="276f8-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="276f8-127">-AddressPrefix</span></span>
<span data-ttu-id="276f8-128">가상 네트워크의 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="276f8-129">-AsJob</span></span>
<span data-ttu-id="276f8-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="276f8-130">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276f8-131">-DefaultProfile</span></span>
<span data-ttu-id="276f8-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="276f8-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="276f8-133">-DnsServer</span></span>
<span data-ttu-id="276f8-134">서브넷에 대 한 DNS 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-134">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="276f8-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="276f8-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="276f8-136">DDoS 보호가 사용 되는지 여부를 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="276f8-137">-EnableVmProtection</span></span>
<span data-ttu-id="276f8-138">Vm 보호가 사용 하도록 설정 되어 있는지 여부를 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-139">-Force</span><span class="sxs-lookup"><span data-stu-id="276f8-139">-Force</span></span>
<span data-ttu-id="276f8-140">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-140">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-141">-위치</span><span class="sxs-lookup"><span data-stu-id="276f8-141">-Location</span></span>
<span data-ttu-id="276f8-142">가상 네트워크의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-142">Specifies the region for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-143">-이름</span><span class="sxs-lookup"><span data-stu-id="276f8-143">-Name</span></span>
<span data-ttu-id="276f8-144">이 cmdlet이 만드는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="276f8-145">-ResourceGroupName</span></span>
<span data-ttu-id="276f8-146">가상 네트워크를 포함할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-146">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-147">-서브넷</span><span class="sxs-lookup"><span data-stu-id="276f8-147">-Subnet</span></span>
<span data-ttu-id="276f8-148">가상 네트워크와 연결할 서브넷 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-148">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-149">태그</span><span class="sxs-lookup"><span data-stu-id="276f8-149">-Tag</span></span>
<span data-ttu-id="276f8-150">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="276f8-151">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="276f8-151">For example:</span></span>

<span data-ttu-id="276f8-152">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="276f8-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-153">-확인</span><span class="sxs-lookup"><span data-stu-id="276f8-153">-Confirm</span></span>
<span data-ttu-id="276f8-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="276f8-155">-WhatIf</span></span>
<span data-ttu-id="276f8-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="276f8-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276f8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276f8-158">CommonParameters</span></span>
<span data-ttu-id="276f8-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="276f8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276f8-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276f8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276f8-161">입력</span><span class="sxs-lookup"><span data-stu-id="276f8-161">INPUTS</span></span>

## <span data-ttu-id="276f8-162">출력</span><span class="sxs-lookup"><span data-stu-id="276f8-162">OUTPUTS</span></span>

### <span data-ttu-id="276f8-163">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="276f8-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="276f8-164">상속자</span><span class="sxs-lookup"><span data-stu-id="276f8-164">NOTES</span></span>

## <span data-ttu-id="276f8-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="276f8-165">RELATED LINKS</span></span>

[<span data-ttu-id="276f8-166">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="276f8-166">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="276f8-167">제거-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="276f8-167">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="276f8-168">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="276f8-168">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)
