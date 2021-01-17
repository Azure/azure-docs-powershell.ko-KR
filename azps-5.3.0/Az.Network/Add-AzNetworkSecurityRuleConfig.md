---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491834"
---
# <span data-ttu-id="1d43a-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d43a-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="1d43a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d43a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d43a-103">네트워크 보안 그룹에 네트워크 보안 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="1d43a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d43a-104">SYNTAX</span></span>

### <span data-ttu-id="1d43a-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d43a-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d43a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d43a-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d43a-107">설명</span><span class="sxs-lookup"><span data-stu-id="1d43a-107">DESCRIPTION</span></span>
<span data-ttu-id="1d43a-108">**Add-AzNetworkSecurityRuleConfig** cmdlet은 Azure 네트워크 보안 그룹에 네트워크 보안 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="1d43a-109">예제</span><span class="sxs-lookup"><span data-stu-id="1d43a-109">EXAMPLES</span></span>

### <span data-ttu-id="1d43a-110">1: 네트워크 보안 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="1d43a-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="1d43a-111">첫 번째 명령은 리소스 그룹 "rg1"에서 "nsg1"이라는 Azure 네트워크 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="1d43a-112">두 번째 명령은 포트 3389의 인터넷에서 검색된 네트워크 보안 그룹 개체로 트래픽을 허용하는 "rdp-rule"이라는 네트워크 보안 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="1d43a-113">수정된 Azure 네트워크 보안 그룹을 유지 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="1d43a-114">2: 애플리케이션 보안 그룹을 통해 새 보안 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="1d43a-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="1d43a-115">먼저 두 개의 새 애플리케이션 보안 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-115">First, we create two new application security groups.</span></span> <span data-ttu-id="1d43a-116">그런 다음 리소스 그룹 "rg1"에서 "nsg1"이라는 Azure 네트워크 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="1d43a-117">"rdp-rule"이라는 네트워크 보안 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="1d43a-118">규칙은 애플리케이션 보안 그룹 "srcAsg"의 모든 IP 구성에서 포트 3389의 "destAsg"의 모든 IP 구성으로 트래픽을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="1d43a-119">규칙을 추가한 후 수정된 Azure 네트워크 보안 그룹을 유지하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="1d43a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d43a-120">PARAMETERS</span></span>

### <span data-ttu-id="1d43a-121">-Access</span><span class="sxs-lookup"><span data-stu-id="1d43a-121">-Access</span></span>
<span data-ttu-id="1d43a-122">네트워크 트래픽을 허용하거나 거부할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="1d43a-123">이 매개 변수에 허용되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d43a-124">-DefaultProfile</span></span>
<span data-ttu-id="1d43a-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d43a-126">-Description</span><span class="sxs-lookup"><span data-stu-id="1d43a-126">-Description</span></span>
<span data-ttu-id="1d43a-127">네트워크 보안 규칙 구성에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1d43a-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="1d43a-129">대상 주소의 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="1d43a-130">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1d43a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d43a-131">CIDR(CIDR(Classless Interdomain Routing)) 주소</span><span class="sxs-lookup"><span data-stu-id="1d43a-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="1d43a-132">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="1d43a-132">A destination IP address range</span></span>
- <span data-ttu-id="1d43a-133">IP 주소와 일치하는 와일드카드 문자(\*)는 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d43a-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="1d43a-135">규칙에 대한 대상으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1d43a-136">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1d43a-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="1d43a-138">규칙에 대한 대상으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1d43a-139">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="1d43a-140">-DestinationPortRange</span></span>
<span data-ttu-id="1d43a-141">대상 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="1d43a-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1d43a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d43a-143">정수</span><span class="sxs-lookup"><span data-stu-id="1d43a-143">An integer</span></span>
- <span data-ttu-id="1d43a-144">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="1d43a-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1d43a-145">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-145">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="1d43a-146">-Direction</span></span>
<span data-ttu-id="1d43a-147">들어오는 트래픽 또는 외출 트래픽에서 규칙이 평가될지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="1d43a-148">이 매개 변수에 허용되는 값은 인바운드 및 아웃바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-149">-Name</span><span class="sxs-lookup"><span data-stu-id="1d43a-149">-Name</span></span>
<span data-ttu-id="1d43a-150">네트워크 보안 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="1d43a-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d43a-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1d43a-152">**NetworkSecurityGroup 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1d43a-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="1d43a-153">이 cmdlet은 이 매개 변수가 지정하는 개체에 네트워크 보안 규칙 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="1d43a-154">-Priority</span></span>
<span data-ttu-id="1d43a-155">규칙 구성의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="1d43a-156">이 매개 변수에 허용되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="1d43a-157">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="1d43a-158">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-158">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1d43a-159">-Protocol</span></span>
<span data-ttu-id="1d43a-160">규칙 구성이 적용되는 네트워크 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="1d43a-161">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1d43a-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d43a-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="1d43a-162">Tcp</span></span>
- <span data-ttu-id="1d43a-163">Udp</span><span class="sxs-lookup"><span data-stu-id="1d43a-163">Udp</span></span>
- <span data-ttu-id="1d43a-164">둘 다 일치할 와일드카드 문자(\*)</span><span class="sxs-lookup"><span data-stu-id="1d43a-164">Wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1d43a-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="1d43a-166">원본 주소의 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="1d43a-167">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1d43a-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d43a-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="1d43a-168">A CIDR</span></span>
- <span data-ttu-id="1d43a-169">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="1d43a-169">A source IP range</span></span>
- <span data-ttu-id="1d43a-170">모든 IP 주소와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="1d43a-171">VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d43a-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="1d43a-173">규칙에 대한 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="1d43a-174">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1d43a-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="1d43a-176">규칙에 대한 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="1d43a-177">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="1d43a-178">-SourcePortRange</span></span>
<span data-ttu-id="1d43a-179">원본 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-179">Specifies a source port or range.</span></span>
<span data-ttu-id="1d43a-180">이 값은 0에서 65535 사이의 범위로 정수로 표현되거나 모든 원본 포트와 일치하기 위해 와일드카드 문자(\*)로 표현됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d43a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d43a-181">CommonParameters</span></span>
<span data-ttu-id="1d43a-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d43a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d43a-183">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d43a-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d43a-184">입력</span><span class="sxs-lookup"><span data-stu-id="1d43a-184">INPUTS</span></span>

### <span data-ttu-id="1d43a-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d43a-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1d43a-186">출력</span><span class="sxs-lookup"><span data-stu-id="1d43a-186">OUTPUTS</span></span>

### <span data-ttu-id="1d43a-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d43a-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1d43a-188">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d43a-188">NOTES</span></span>

## <span data-ttu-id="1d43a-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d43a-189">RELATED LINKS</span></span>

[<span data-ttu-id="1d43a-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d43a-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d43a-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d43a-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d43a-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d43a-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d43a-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d43a-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


