---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 45702774e44e4b3da0b90d37e86e478c52dcba17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953920"
---
# <span data-ttu-id="b6e3c-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6e3c-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b6e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e3c-103">네트워크 보안 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="b6e3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6e3c-104">SYNTAX</span></span>

### <span data-ttu-id="b6e3c-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6e3c-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6e3c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e3c-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6e3c-107">설명</span><span class="sxs-lookup"><span data-stu-id="b6e3c-107">DESCRIPTION</span></span>
<span data-ttu-id="b6e3c-108">**New-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대한 Azure 네트워크 보안 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="b6e3c-109">예제</span><span class="sxs-lookup"><span data-stu-id="b6e3c-109">EXAMPLES</span></span>

### <span data-ttu-id="b6e3c-110">예제 1: RDP를 허용하는 네트워크 보안 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="b6e3c-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="b6e3c-111">이 명령은 인터넷에서 포트 3389로 액세스를 허용하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="b6e3c-112">예제 2: HTTP를 허용하는 네트워크 보안 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="b6e3c-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="b6e3c-113">이 명령은 인터넷에서 포트 80으로의 액세스를 허용하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="b6e3c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6e3c-114">PARAMETERS</span></span>

### <span data-ttu-id="b6e3c-115">-Access</span><span class="sxs-lookup"><span data-stu-id="b6e3c-115">-Access</span></span>
<span data-ttu-id="b6e3c-116">네트워크 트래픽을 허용하거나 거부할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="b6e3c-117">이 매개 변수에 대해 허용되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="b6e3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e3c-118">-DefaultProfile</span></span>
<span data-ttu-id="b6e3c-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6e3c-120">-Description</span><span class="sxs-lookup"><span data-stu-id="b6e3c-120">-Description</span></span>
<span data-ttu-id="b6e3c-121">만들 네트워크 보안 규칙 구성에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="b6e3c-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6e3c-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="b6e3c-123">대상 주소 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="b6e3c-124">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6e3c-125">CIDR(CIDR(Classless Interdomain Routing)) 주소</span><span class="sxs-lookup"><span data-stu-id="b6e3c-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="b6e3c-126">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="b6e3c-126">A destination IP address range</span></span> 
- <span data-ttu-id="b6e3c-127">모든 IP 주소와 일치하기 위한 와일드카드 문자(\*)를 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="b6e3c-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6e3c-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="b6e3c-129">애플리케이션 보안 그룹은 규칙의 대상으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b6e3c-130">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b6e3c-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b6e3c-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="b6e3c-132">애플리케이션 보안 그룹은 규칙의 대상으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b6e3c-133">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b6e3c-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="b6e3c-134">-DestinationPortRange</span></span>
<span data-ttu-id="b6e3c-135">대상 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="b6e3c-136">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6e3c-137">정수</span><span class="sxs-lookup"><span data-stu-id="b6e3c-137">An integer</span></span>
- <span data-ttu-id="b6e3c-138">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="b6e3c-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b6e3c-139">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b6e3c-140">-방향</span><span class="sxs-lookup"><span data-stu-id="b6e3c-140">-Direction</span></span>
<span data-ttu-id="b6e3c-141">들어오는 트래픽 또는 외출 트래픽에 대해 규칙이 평가될지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="b6e3c-142">이 매개 변수에 대해 허용되는 값은 인바운드 및 아웃바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="b6e3c-143">-Name</span><span class="sxs-lookup"><span data-stu-id="b6e3c-143">-Name</span></span>
<span data-ttu-id="b6e3c-144">이 cmdlet에서 만드는 네트워크 보안 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b6e3c-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="b6e3c-145">-Priority</span></span>
<span data-ttu-id="b6e3c-146">규칙 구성의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="b6e3c-147">이 매개 변수에 허용되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="b6e3c-148">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="b6e3c-149">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높아진다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="b6e3c-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b6e3c-150">-Protocol</span></span>
<span data-ttu-id="b6e3c-151">새 규칙 구성이 적용되는 네트워크 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="b6e3c-152">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6e3c-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="b6e3c-153">Tcp</span></span>
- <span data-ttu-id="b6e3c-154">Udp</span><span class="sxs-lookup"><span data-stu-id="b6e3c-154">Udp</span></span>
- <span data-ttu-id="b6e3c-155">와일드카드 문자(\*)를 모두 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="b6e3c-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6e3c-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="b6e3c-157">원본 주소 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="b6e3c-158">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6e3c-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="b6e3c-159">A CIDR</span></span>
- <span data-ttu-id="b6e3c-160">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="b6e3c-160">A source IP range</span></span>
- <span data-ttu-id="b6e3c-161">모든 IP 주소와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="b6e3c-162">VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="b6e3c-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6e3c-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="b6e3c-164">규칙의 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="b6e3c-165">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b6e3c-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b6e3c-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="b6e3c-167">규칙의 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="b6e3c-168">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b6e3c-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="b6e3c-169">-SourcePortRange</span></span>
<span data-ttu-id="b6e3c-170">원본 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-170">Specifies the source port or range.</span></span>
<span data-ttu-id="b6e3c-171">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6e3c-172">정수</span><span class="sxs-lookup"><span data-stu-id="b6e3c-172">An integer</span></span>
- <span data-ttu-id="b6e3c-173">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="b6e3c-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b6e3c-174">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b6e3c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e3c-175">CommonParameters</span></span>
<span data-ttu-id="b6e3c-176">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e3c-177">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e3c-178">입력</span><span class="sxs-lookup"><span data-stu-id="b6e3c-178">INPUTS</span></span>

### <span data-ttu-id="b6e3c-179">없음</span><span class="sxs-lookup"><span data-stu-id="b6e3c-179">None</span></span>

## <span data-ttu-id="b6e3c-180">출력</span><span class="sxs-lookup"><span data-stu-id="b6e3c-180">OUTPUTS</span></span>

### <span data-ttu-id="b6e3c-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="b6e3c-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="b6e3c-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6e3c-182">NOTES</span></span>

## <span data-ttu-id="b6e3c-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6e3c-183">RELATED LINKS</span></span>

[<span data-ttu-id="b6e3c-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6e3c-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b6e3c-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6e3c-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b6e3c-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6e3c-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b6e3c-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6e3c-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


