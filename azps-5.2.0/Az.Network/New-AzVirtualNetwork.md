---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333362"
---
# <span data-ttu-id="533e7-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="533e7-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="533e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="533e7-102">SYNOPSIS</span></span>
<span data-ttu-id="533e7-103">가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-103">Creates a virtual network.</span></span>

## <span data-ttu-id="533e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="533e7-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="533e7-105">설명</span><span class="sxs-lookup"><span data-stu-id="533e7-105">DESCRIPTION</span></span>
<span data-ttu-id="533e7-106">**New-AzVirtualNetwork** cmdlet은 Azure 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="533e7-107">예제</span><span class="sxs-lookup"><span data-stu-id="533e7-107">EXAMPLES</span></span>

### <span data-ttu-id="533e7-108">예제 1: 두 개의 서브넷이 있는 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="533e7-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="533e7-109">이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="533e7-110">먼저 중앙 지역에 새 리소스 그룹이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="533e7-111">그런 다음, 이 예제에서는 두 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="533e7-112">New-AzVirtualNetworkSubnetConfig cmdlet은 서버 쪽에서 서브넷을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="533e7-113">frontendSubnet이라는 하나의 서브넷과 backendSubnet이라는 서브넷이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="533e7-114">그런 New-AzVirtualNetwork cmdlet은 CIDR 10.0.0.0/16을 주소 연결 및 두 개의 서브넷으로 사용하여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="533e7-115">예제 2: DNS 설정을 사용하여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="533e7-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="533e7-116">이 예제에서는 두 개의 서브넷과 두 개의 DNS 서버가 있는 가상 네트워크를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="533e7-117">가상 네트워크에 DNS 서버를 지정하면 이 가상 네트워크에 배포된 NIC/VM이 이러한 DNS 서버를 기본값으로 상속합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="533e7-118">이러한 기본값은 NIC 수준 설정을 통해 NIC당 덮어질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="533e7-119">VNET에 DNS 서버가 지정되지 않은 경우 NI에 DNS 서버가 없는 경우 DNS 확인에 기본 Azure DNS 서버가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="533e7-120">예제 3: 네트워크 보안 그룹을 참조하는 서브넷이 있는 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="533e7-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="533e7-121">이 예제에서는 네트워크 보안 그룹을 참조하는 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="533e7-122">먼저, 이 예제에서는 만들 리소스에 대한 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="533e7-123">그런 다음 인바운드 RDP 액세스를 허용하지만 그렇지 않으면 기본 네트워크 보안 그룹 규칙을 적용하는 네트워크 보안 그룹이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="533e7-124">그런 New-AzVirtualNetworkSubnetConfig cmdlet은 생성된 네트워크 보안 그룹을 참조하는 두 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="533e7-125">그런 New-AzVirtualNetwork 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="533e7-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="533e7-126">PARAMETERS</span></span>

### <span data-ttu-id="533e7-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="533e7-127">-AddressPrefix</span></span>
<span data-ttu-id="533e7-128">가상 네트워크에 대한 IP 주소 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="533e7-129">-AsJob</span></span>
<span data-ttu-id="533e7-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="533e7-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="533e7-131">-BgpCommunity</span></span>
<span data-ttu-id="533e7-132">ExpressRoute를 통해 보급된 BGP 커뮤니티입니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="533e7-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="533e7-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="533e7-134">가상 네트워크와 연결된 DDoS 보호 계획 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="533e7-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533e7-135">-DefaultProfile</span></span>
<span data-ttu-id="533e7-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="533e7-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="533e7-137">-DnsServer</span></span>
<span data-ttu-id="533e7-138">서브넷에 대한 DNS 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="533e7-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="533e7-139">-EnableDdosProtection</span></span>
<span data-ttu-id="533e7-140">DDoS 보호를 사용하도록 설정하는지 아니면 그렇지 않은지 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-141">-Force</span><span class="sxs-lookup"><span data-stu-id="533e7-141">-Force</span></span>
<span data-ttu-id="533e7-142">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-142">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="533e7-143">-IpAllocation</span></span>
<span data-ttu-id="533e7-144">가상 네트워크에 대한 IpAllocations를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-145">-Location</span><span class="sxs-lookup"><span data-stu-id="533e7-145">-Location</span></span>
<span data-ttu-id="533e7-146">가상 네트워크에 대한 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-146">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-147">-Name</span><span class="sxs-lookup"><span data-stu-id="533e7-147">-Name</span></span>
<span data-ttu-id="533e7-148">이 cmdlet에서 만드는 가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="533e7-149">-ResourceGroupName</span></span>
<span data-ttu-id="533e7-150">가상 네트워크를 포함할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-150">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-151">-Subnet</span><span class="sxs-lookup"><span data-stu-id="533e7-151">-Subnet</span></span>
<span data-ttu-id="533e7-152">가상 네트워크와 연결하기 위한 서브넷 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="533e7-153">-Tag</span></span>
<span data-ttu-id="533e7-154">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="533e7-155">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="533e7-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="533e7-156">-Confirm</span></span>
<span data-ttu-id="533e7-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="533e7-158">-WhatIf</span></span>
<span data-ttu-id="533e7-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="533e7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="533e7-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533e7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533e7-161">CommonParameters</span></span>
<span data-ttu-id="533e7-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="533e7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533e7-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="533e7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533e7-164">입력</span><span class="sxs-lookup"><span data-stu-id="533e7-164">INPUTS</span></span>

### <span data-ttu-id="533e7-165">System.String</span><span class="sxs-lookup"><span data-stu-id="533e7-165">System.String</span></span>

### <span data-ttu-id="533e7-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="533e7-166">System.String[]</span></span>

### <span data-ttu-id="533e7-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="533e7-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="533e7-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="533e7-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="533e7-169">출력</span><span class="sxs-lookup"><span data-stu-id="533e7-169">OUTPUTS</span></span>

### <span data-ttu-id="533e7-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="533e7-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="533e7-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="533e7-171">NOTES</span></span>

## <span data-ttu-id="533e7-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="533e7-172">RELATED LINKS</span></span>

[<span data-ttu-id="533e7-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="533e7-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="533e7-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="533e7-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="533e7-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="533e7-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="533e7-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="533e7-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
