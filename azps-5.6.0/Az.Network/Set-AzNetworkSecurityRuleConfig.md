---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003275"
---
# <span data-ttu-id="576a4-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="576a4-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="576a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576a4-102">SYNOPSIS</span></span>
<span data-ttu-id="576a4-103">네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="576a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="576a4-104">SYNTAX</span></span>

### <span data-ttu-id="576a4-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="576a4-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="576a4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="576a4-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="576a4-107">설명</span><span class="sxs-lookup"><span data-stu-id="576a4-107">DESCRIPTION</span></span>
<span data-ttu-id="576a4-108">**Set-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="576a4-109">예제</span><span class="sxs-lookup"><span data-stu-id="576a4-109">EXAMPLES</span></span>

### <span data-ttu-id="576a4-110">예제 1: 네트워크 보안 규칙에서 액세스 구성 변경</span><span class="sxs-lookup"><span data-stu-id="576a4-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="576a4-111">첫 번째 명령은 NSG-FrontEnd라는 네트워크 보안 그룹을 한 다음, 변수에 $nsg.</span><span class="sxs-lookup"><span data-stu-id="576a4-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="576a4-112">두 번째 명령은 파이프라인 연산자를 사용하여 rdp-rule라는 보안 규칙 구성을 $nsg Get-AzNetworkSecurityRuleConfig에 보안 그룹을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="576a4-113">세 번째 명령은 rdp-rule의 액세스 구성을 거부로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="576a4-114">그러나 이 규칙은 규칙을 덮어 우고 함수 함수에 전달되는 매개 변수만 Set-AzNetworkSecurityRuleConfig 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="576a4-115">참고: 단일 특성을 변경할 수 있는 방법은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="576a4-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="576a4-116">Example 2</span></span>

<span data-ttu-id="576a4-117">네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="576a4-118">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="576a4-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="576a4-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="576a4-119">PARAMETERS</span></span>

### <span data-ttu-id="576a4-120">-Access</span><span class="sxs-lookup"><span data-stu-id="576a4-120">-Access</span></span>
<span data-ttu-id="576a4-121">네트워크 트래픽을 허용하거나 거부할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="576a4-122">이 매개 변수에 대해 허용되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="576a4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576a4-123">-DefaultProfile</span></span>
<span data-ttu-id="576a4-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576a4-125">-Description</span><span class="sxs-lookup"><span data-stu-id="576a4-125">-Description</span></span>
<span data-ttu-id="576a4-126">규칙 구성에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="576a4-127">최대 크기는 140자입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="576a4-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="576a4-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="576a4-129">대상 주소 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="576a4-130">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="576a4-131">CIDR(CIDR(Classless Interdomain Routing)) 주소</span><span class="sxs-lookup"><span data-stu-id="576a4-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="576a4-132">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="576a4-132">A destination IP address range</span></span> 
- <span data-ttu-id="576a4-133">모든 IP 주소와 일치하기 위한 와일드카드 문자(\*)를 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="576a4-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="576a4-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="576a4-135">애플리케이션 보안 그룹은 규칙의 대상으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="576a4-136">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="576a4-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="576a4-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="576a4-138">애플리케이션 보안 그룹은 규칙의 대상으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="576a4-139">'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="576a4-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="576a4-140">-DestinationPortRange</span></span>
<span data-ttu-id="576a4-141">대상 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="576a4-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="576a4-143">정수</span><span class="sxs-lookup"><span data-stu-id="576a4-143">An integer</span></span> 
- <span data-ttu-id="576a4-144">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="576a4-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="576a4-145">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="576a4-146">-방향</span><span class="sxs-lookup"><span data-stu-id="576a4-146">-Direction</span></span>
<span data-ttu-id="576a4-147">들어오는 트래픽 또는 외출 트래픽에 대해 규칙이 평가될지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="576a4-148">이 매개 변수에 대해 허용되는 값은 인바운드 및 아웃바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="576a4-149">-Name</span><span class="sxs-lookup"><span data-stu-id="576a4-149">-Name</span></span>
<span data-ttu-id="576a4-150">이 cmdlet에서 설정하는 네트워크 보안 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="576a4-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="576a4-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="576a4-152">설정할 네트워크 보안 규칙 구성을 포함하는 **NetworkSecurityGroup** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="576a4-153">-Priority</span><span class="sxs-lookup"><span data-stu-id="576a4-153">-Priority</span></span>
<span data-ttu-id="576a4-154">규칙 구성의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="576a4-155">이 매개 변수에 대해 허용되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="576a4-156">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="576a4-157">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높아진다.</span><span class="sxs-lookup"><span data-stu-id="576a4-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="576a4-158">-Protocol</span><span class="sxs-lookup"><span data-stu-id="576a4-158">-Protocol</span></span>
<span data-ttu-id="576a4-159">규칙 구성이 적용되는 네트워크 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="576a4-160">이 매개 변수에 대해 허용되는 값은 ---Tcp입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="576a4-161">Udp</span><span class="sxs-lookup"><span data-stu-id="576a4-161">Udp</span></span>
- <span data-ttu-id="576a4-162">둘 다 일치할 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="576a4-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="576a4-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="576a4-164">원본 주소 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="576a4-165">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="576a4-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="576a4-166">A CIDR</span></span>
- <span data-ttu-id="576a4-167">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="576a4-167">A source IP range</span></span>
- <span data-ttu-id="576a4-168">모든 IP 주소와 일치하는 와일드카드 문자(\*)를 가상Network, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="576a4-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="576a4-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="576a4-170">규칙의 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="576a4-171">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="576a4-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="576a4-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="576a4-173">규칙의 원본으로 설정된 애플리케이션 보안 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="576a4-174">'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="576a4-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="576a4-175">-SourcePortRange</span></span>
<span data-ttu-id="576a4-176">원본 포트 또는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-176">Specifies the source port or range.</span></span>
<span data-ttu-id="576a4-177">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="576a4-178">정수</span><span class="sxs-lookup"><span data-stu-id="576a4-178">An integer</span></span>
- <span data-ttu-id="576a4-179">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="576a4-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="576a4-180">모든 포트와 일치하는 와일드카드 문자(\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="576a4-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576a4-181">CommonParameters</span></span>
<span data-ttu-id="576a4-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="576a4-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576a4-183">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="576a4-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576a4-184">입력</span><span class="sxs-lookup"><span data-stu-id="576a4-184">INPUTS</span></span>

### <span data-ttu-id="576a4-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="576a4-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="576a4-186">출력</span><span class="sxs-lookup"><span data-stu-id="576a4-186">OUTPUTS</span></span>

### <span data-ttu-id="576a4-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="576a4-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="576a4-188">참고 사항</span><span class="sxs-lookup"><span data-stu-id="576a4-188">NOTES</span></span>

## <span data-ttu-id="576a4-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="576a4-189">RELATED LINKS</span></span>

[<span data-ttu-id="576a4-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="576a4-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="576a4-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="576a4-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="576a4-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="576a4-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="576a4-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="576a4-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


