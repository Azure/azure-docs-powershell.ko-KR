---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: b2b1667a9326a9c25d78639e397146c0dd85dc5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875663"
---
# <span data-ttu-id="82aee-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82aee-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="82aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82aee-102">SYNOPSIS</span></span>
<span data-ttu-id="82aee-103">네트워크 보안 규칙 구성을 네트워크 보안 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="82aee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82aee-104">SYNTAX</span></span>

### <span data-ttu-id="82aee-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="82aee-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82aee-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="82aee-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82aee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="82aee-107">DESCRIPTION</span></span>
<span data-ttu-id="82aee-108">**추가-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 규칙 구성을 Azure 네트워크 보안 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="82aee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="82aee-109">EXAMPLES</span></span>

### <span data-ttu-id="82aee-110">1: 네트워크 보안 그룹 추가</span><span class="sxs-lookup"><span data-stu-id="82aee-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="82aee-111">첫 번째 명령은 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="82aee-112">두 번째 명령은 포트 3389의 인터넷에서 검색 된 네트워크 보안 그룹 개체에 트래픽을 허용 하는 "rdp-tcp" 라는 네트워크 보안 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="82aee-113">수정 된 Azure 네트워크 보안 그룹을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="82aee-114">1: 응용 프로그램 보안 그룹을 사용 하 여 새 보안 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="82aee-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="82aee-115">먼저 두 가지 새로운 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-115">First, we create two new application security groups.</span></span> <span data-ttu-id="82aee-116">그런 다음 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="82aee-117">".rdp-rule" 이라는 네트워크 보안 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="82aee-118">이 규칙은 응용 프로그램 보안 그룹 "srcAsg"의 모든 IP 구성에서 포트 3389에 있는 "destAsg"의 모든 IP 구성에 대 한 트래픽을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="82aee-119">규칙을 추가한 후에는 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="82aee-120">변수</span><span class="sxs-lookup"><span data-stu-id="82aee-120">PARAMETERS</span></span>

### <span data-ttu-id="82aee-121">-Access</span><span class="sxs-lookup"><span data-stu-id="82aee-121">-Access</span></span>
<span data-ttu-id="82aee-122">네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="82aee-123">이 매개 변수에 허용 되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82aee-124">-DefaultProfile</span></span>
<span data-ttu-id="82aee-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82aee-126">-설명</span><span class="sxs-lookup"><span data-stu-id="82aee-126">-Description</span></span>
<span data-ttu-id="82aee-127">네트워크 보안 규칙 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="82aee-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="82aee-129">대상 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="82aee-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82aee-131">클래스 없는 도메인간 라우팅 (CIDR) 주소</span><span class="sxs-lookup"><span data-stu-id="82aee-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="82aee-132">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="82aee-132">A destination IP address range</span></span>
- <span data-ttu-id="82aee-133">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="82aee-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="82aee-134">VirtualNetwork, AzureLoadBalancer, 인터넷 등의 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82aee-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="82aee-136">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="82aee-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="82aee-137">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="82aee-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="82aee-139">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="82aee-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="82aee-140">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="82aee-141">-DestinationPortRange</span></span>
<span data-ttu-id="82aee-142">대상 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="82aee-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82aee-144">정수</span><span class="sxs-lookup"><span data-stu-id="82aee-144">An integer</span></span>
- <span data-ttu-id="82aee-145">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="82aee-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="82aee-146">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="82aee-146">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-147">방향</span><span class="sxs-lookup"><span data-stu-id="82aee-147">-Direction</span></span>
<span data-ttu-id="82aee-148">들어오는 트래픽이나 보내는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="82aee-149">이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-150">-이름</span><span class="sxs-lookup"><span data-stu-id="82aee-150">-Name</span></span>
<span data-ttu-id="82aee-151">네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-151">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="82aee-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82aee-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="82aee-153">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="82aee-154">이 cmdlet은이 매개 변수에서 지정 하는 개체에 네트워크 보안 규칙 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-155">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="82aee-155">-Priority</span></span>
<span data-ttu-id="82aee-156">규칙 구성의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="82aee-157">이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="82aee-158">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="82aee-159">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-159">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-160">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="82aee-160">-Protocol</span></span>
<span data-ttu-id="82aee-161">규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="82aee-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82aee-163">Net.tcp</span><span class="sxs-lookup"><span data-stu-id="82aee-163">Tcp</span></span>
- <span data-ttu-id="82aee-164">Udp</span><span class="sxs-lookup"><span data-stu-id="82aee-164">Udp</span></span>
- <span data-ttu-id="82aee-165">와일드 카드 문자 (\*)와 일치 하는 항목</span><span class="sxs-lookup"><span data-stu-id="82aee-165">Wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="82aee-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="82aee-167">원본 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="82aee-168">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="82aee-169">CIDR</span><span class="sxs-lookup"><span data-stu-id="82aee-169">A CIDR</span></span>
- <span data-ttu-id="82aee-170">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="82aee-170">A source IP range</span></span>
- <span data-ttu-id="82aee-171">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="82aee-172">VirtualNetwork, AzureLoadBalancer 및 Internet 등의 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82aee-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="82aee-174">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="82aee-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="82aee-175">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="82aee-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="82aee-177">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="82aee-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="82aee-178">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="82aee-179">-SourcePortRange</span></span>
<span data-ttu-id="82aee-180">원본 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-180">Specifies a source port or range.</span></span>
<span data-ttu-id="82aee-181">이 값은 정수 (0에서 65535 사이의 범위 또는 원본 포트와 일치 하는 와일드 카드 문자 (\*))로 표현 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aee-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82aee-182">CommonParameters</span></span>
<span data-ttu-id="82aee-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82aee-184">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82aee-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82aee-185">입력</span><span class="sxs-lookup"><span data-stu-id="82aee-185">INPUTS</span></span>

### <span data-ttu-id="82aee-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82aee-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="82aee-187">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="82aee-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="82aee-188">출력</span><span class="sxs-lookup"><span data-stu-id="82aee-188">OUTPUTS</span></span>

### <span data-ttu-id="82aee-189">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82aee-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="82aee-190">상속자</span><span class="sxs-lookup"><span data-stu-id="82aee-190">NOTES</span></span>

## <span data-ttu-id="82aee-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82aee-191">RELATED LINKS</span></span>

[<span data-ttu-id="82aee-192">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82aee-192">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="82aee-193">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82aee-193">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="82aee-194">제거-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82aee-194">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="82aee-195">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82aee-195">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


