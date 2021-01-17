---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371575"
---
# <span data-ttu-id="91347-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91347-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="91347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91347-102">SYNOPSIS</span></span>
<span data-ttu-id="91347-103">네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="91347-104">구문</span><span class="sxs-lookup"><span data-stu-id="91347-104">SYNTAX</span></span>

### <span data-ttu-id="91347-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="91347-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91347-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91347-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91347-107">설명</span><span class="sxs-lookup"><span data-stu-id="91347-107">DESCRIPTION</span></span>
<span data-ttu-id="91347-108">**Set-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="91347-109">예제</span><span class="sxs-lookup"><span data-stu-id="91347-109">EXAMPLES</span></span>

### <span data-ttu-id="91347-110">예제 1: 네트워크 보안 규칙에서 액세스 구성 변경</span><span class="sxs-lookup"><span data-stu-id="91347-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="91347-111">첫 번째 명령은 NSG-FrontEnd라는 네트워크 보안 그룹을 인용한 다음, NSG-FrontEnd의 변수에 $nsg.</span><span class="sxs-lookup"><span data-stu-id="91347-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="91347-112">두 번째 명령은 파이프라인 연산자를 사용하여 rdp-rule이라는 보안 규칙 구성을 $nsg Get-AzNetworkSecurityRuleConfig에 보안 그룹을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="91347-113">세 번째 명령은 rdp-rule의 액세스 구성을 거부로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="91347-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="91347-114">Example 2</span></span>

<span data-ttu-id="91347-115">네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="91347-116">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="91347-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="91347-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91347-117">PARAMETERS</span></span>

### <span data-ttu-id="91347-118">-Access</span><span class="sxs-lookup"><span data-stu-id="91347-118">-Access</span></span>
<span data-ttu-id="91347-119">네트워크 트래픽을 허용하거나 거부할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="91347-120">이 매개 변수에 허용되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="91347-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91347-121">-DefaultProfile</span></span>
<span data-ttu-id="91347-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91347-123">-Description</span><span class="sxs-lookup"><span data-stu-id="91347-123">-Description</span></span>
<span data-ttu-id="91347-124">규칙 구성에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="91347-125">최대 크기는 140자입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="91347-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="91347-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="91347-127">대상 주소의 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="91347-128">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91347-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91347-129">CIDR(CIDR(Classless Interdomain Routing)) 주소</span><span class="sxs-lookup"><span data-stu-id="91347-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="91347-130">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="91347-130">A destination IP address range</span></span> 
- <span data-ttu-id="91347-131">IP 주소와 일치하는 와일드카드 문자(\*)는 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91347-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="91347-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91347-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="91347-133">규칙에 대한 대상으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="91347-134">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91347-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="91347-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="91347-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="91347-136">규칙에 대한 대상으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="91347-137">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91347-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="91347-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="91347-138">-DestinationPortRange</span></span>
<span data-ttu-id="91347-139">대상 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="91347-140">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91347-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91347-141">정수</span><span class="sxs-lookup"><span data-stu-id="91347-141">An integer</span></span> 
- <span data-ttu-id="91347-142">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="91347-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="91347-143">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="91347-144">-Direction</span><span class="sxs-lookup"><span data-stu-id="91347-144">-Direction</span></span>
<span data-ttu-id="91347-145">들어오는 트래픽 또는 외출 트래픽에 대해 규칙이 평가될지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="91347-146">이 매개 변수에 허용되는 값은 인바운드 및 아웃바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="91347-147">-Name</span><span class="sxs-lookup"><span data-stu-id="91347-147">-Name</span></span>
<span data-ttu-id="91347-148">이 cmdlet이 설정하는 네트워크 보안 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="91347-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91347-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="91347-150">설정할 네트워크 보안 규칙 구성을 포함하는 **NetworkSecurityGroup** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="91347-151">-Priority</span><span class="sxs-lookup"><span data-stu-id="91347-151">-Priority</span></span>
<span data-ttu-id="91347-152">규칙 구성의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="91347-153">이 매개 변수에 허용되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="91347-154">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="91347-155">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="91347-156">-Protocol</span><span class="sxs-lookup"><span data-stu-id="91347-156">-Protocol</span></span>
<span data-ttu-id="91347-157">규칙 구성이 적용되는 네트워크 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="91347-158">이 매개 변수에 허용되는 값은 --Tcp입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="91347-159">Udp</span><span class="sxs-lookup"><span data-stu-id="91347-159">Udp</span></span>
- <span data-ttu-id="91347-160">둘 다 일치할 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="91347-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="91347-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="91347-162">원본 주소의 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="91347-163">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91347-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91347-164">A CIDR</span><span class="sxs-lookup"><span data-stu-id="91347-164">A CIDR</span></span>
- <span data-ttu-id="91347-165">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="91347-165">A source IP range</span></span>
- <span data-ttu-id="91347-166">IP 주소와 일치하는 와일드카드 문자(\*)를 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91347-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="91347-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91347-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="91347-168">규칙에 대한 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="91347-169">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91347-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="91347-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="91347-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="91347-171">규칙에 대한 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="91347-172">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91347-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="91347-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="91347-173">-SourcePortRange</span></span>
<span data-ttu-id="91347-174">원본 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-174">Specifies the source port or range.</span></span>
<span data-ttu-id="91347-175">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91347-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91347-176">정수</span><span class="sxs-lookup"><span data-stu-id="91347-176">An integer</span></span>
- <span data-ttu-id="91347-177">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="91347-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="91347-178">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="91347-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="91347-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91347-179">CommonParameters</span></span>
<span data-ttu-id="91347-180">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91347-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91347-181">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="91347-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91347-182">입력</span><span class="sxs-lookup"><span data-stu-id="91347-182">INPUTS</span></span>

### <span data-ttu-id="91347-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91347-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="91347-184">출력</span><span class="sxs-lookup"><span data-stu-id="91347-184">OUTPUTS</span></span>

### <span data-ttu-id="91347-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="91347-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="91347-186">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91347-186">NOTES</span></span>

## <span data-ttu-id="91347-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91347-187">RELATED LINKS</span></span>

[<span data-ttu-id="91347-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91347-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="91347-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91347-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="91347-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91347-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="91347-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="91347-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


