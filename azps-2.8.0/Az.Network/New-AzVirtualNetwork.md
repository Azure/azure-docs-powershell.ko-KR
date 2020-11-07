---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 3948161bcc4f9f92f95e7669fb543cd8e00b34d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871341"
---
# <span data-ttu-id="e7f64-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7f64-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="e7f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f64-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f64-103">가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-103">Creates a virtual network.</span></span>

## <span data-ttu-id="e7f64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7f64-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7f64-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f64-106">**새 AzVirtualNetwork** Cmdlet은 Azure 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="e7f64-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7f64-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f64-108">1: 서브넷 두 개를 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="e7f64-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="e7f64-109">이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="e7f64-110">먼저 새 리소스 그룹이 centralus 지역에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="e7f64-111">그런 다음이 예제는 두 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="e7f64-112">New-AzVirtualNetworkSubnetConfig cmdlet은 서버 쪽에 서브넷을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="e7f64-113">FrontendSubnet 라는 서브넷과 backendSubnet 라는 서브넷 하나가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="e7f64-114">그런 다음 New-AzVirtualNetwork cmdlet은 CIDR 10.0.0.0/16을 주소 접두사와 두 개의 서브넷으로 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="e7f64-115">2: DNS 설정을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="e7f64-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="e7f64-116">이 예제에서는 서브넷 2 개와 DNS 서버 두 개를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="e7f64-117">가상 네트워크에서 DNS 서버를 지정 하는 효과는이 가상 네트워크에 배포 된 Nic/Vm이이 DNS 서버를 기본값으로 상속 한다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="e7f64-118">이러한 기본값은 nic 수준 설정을 통해 NIC 별로 덮어쓸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="e7f64-119">VNET에 dns 서버가 지정 되지 않고 Nic에 DNS 서버가 없으면 기본 Azure DNS 서버가 DNS 확인에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="e7f64-120">3: 네트워크 보안 그룹을 참조 하는 서브넷을 사용 하 여 가상 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="e7f64-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="e7f64-121">이 예제에서는 네트워크 보안 그룹을 참조 하는 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="e7f64-122">먼저,이 예제에서는 만들려는 리소스에 대 한 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="e7f64-123">그런 다음 인바운드 RDP 액세스를 허용 하는 네트워크 보안 그룹을 만들지만, 그렇지 않은 경우에는 기본 네트워크 보안 그룹 규칙을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="e7f64-124">그런 다음 New-AzVirtualNetworkSubnetConfig cmdlet은 생성 된 네트워크 보안 그룹을 둘 다 참조 하는 두 서브넷의 메모리 내 표현을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="e7f64-125">그런 다음 New-AzVirtualNetwork 명령은 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="e7f64-126">변수</span><span class="sxs-lookup"><span data-stu-id="e7f64-126">PARAMETERS</span></span>

### <span data-ttu-id="e7f64-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7f64-127">-AddressPrefix</span></span>
<span data-ttu-id="e7f64-128">가상 네트워크의 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="e7f64-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7f64-129">-AsJob</span></span>
<span data-ttu-id="e7f64-130">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e7f64-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7f64-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="e7f64-131">-BgpCommunity</span></span>
<span data-ttu-id="e7f64-132">Express 경로를 통해 광고 된 BGP 커뮤니티입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="e7f64-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="e7f64-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="e7f64-134">가상 네트워크와 연결 된 DDoS protection 계획 리소스에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="e7f64-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f64-135">-DefaultProfile</span></span>
<span data-ttu-id="e7f64-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f64-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="e7f64-137">-DnsServer</span></span>
<span data-ttu-id="e7f64-138">서브넷에 대 한 DNS 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="e7f64-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="e7f64-139">-EnableDdosProtection</span></span>
<span data-ttu-id="e7f64-140">DDoS 보호가 사용 되는지 여부를 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="e7f64-141">-Force</span><span class="sxs-lookup"><span data-stu-id="e7f64-141">-Force</span></span>
<span data-ttu-id="e7f64-142">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7f64-143">-위치</span><span class="sxs-lookup"><span data-stu-id="e7f64-143">-Location</span></span>
<span data-ttu-id="e7f64-144">가상 네트워크의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-144">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="e7f64-145">-이름</span><span class="sxs-lookup"><span data-stu-id="e7f64-145">-Name</span></span>
<span data-ttu-id="e7f64-146">이 cmdlet이 만드는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-146">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7f64-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f64-147">-ResourceGroupName</span></span>
<span data-ttu-id="e7f64-148">가상 네트워크를 포함할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-148">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="e7f64-149">-서브넷</span><span class="sxs-lookup"><span data-stu-id="e7f64-149">-Subnet</span></span>
<span data-ttu-id="e7f64-150">가상 네트워크와 연결할 서브넷 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-150">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="e7f64-151">태그</span><span class="sxs-lookup"><span data-stu-id="e7f64-151">-Tag</span></span>
<span data-ttu-id="e7f64-152">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-152">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7f64-153">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e7f64-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e7f64-154">-확인</span><span class="sxs-lookup"><span data-stu-id="e7f64-154">-Confirm</span></span>
<span data-ttu-id="e7f64-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f64-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f64-156">-WhatIf</span></span>
<span data-ttu-id="e7f64-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f64-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f64-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f64-159">CommonParameters</span></span>
<span data-ttu-id="e7f64-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f64-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f64-161">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f64-161">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f64-162">입력</span><span class="sxs-lookup"><span data-stu-id="e7f64-162">INPUTS</span></span>

### <span data-ttu-id="e7f64-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e7f64-163">System.String</span></span>

### <span data-ttu-id="e7f64-164">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e7f64-164">System.String[]</span></span>

### <span data-ttu-id="e7f64-165">Microsoft. \* PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="e7f64-165">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="e7f64-166">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e7f64-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7f64-167">출력</span><span class="sxs-lookup"><span data-stu-id="e7f64-167">OUTPUTS</span></span>

### <span data-ttu-id="e7f64-168">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e7f64-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e7f64-169">상속자</span><span class="sxs-lookup"><span data-stu-id="e7f64-169">NOTES</span></span>

## <span data-ttu-id="e7f64-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7f64-170">RELATED LINKS</span></span>

[<span data-ttu-id="e7f64-171">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7f64-171">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e7f64-172">제거-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7f64-172">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="e7f64-173">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7f64-173">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="e7f64-174">새로운 AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e7f64-174">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
