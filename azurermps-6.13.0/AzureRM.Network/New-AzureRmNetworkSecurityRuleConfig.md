---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 0950e09185783f0b352defafb7673a2f97461c74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537568"
---
# <span data-ttu-id="39203-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39203-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="39203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39203-102">SYNOPSIS</span></span>
<span data-ttu-id="39203-103">네트워크 보안 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39203-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39203-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39203-104">SYNTAX</span></span>

### <span data-ttu-id="39203-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="39203-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39203-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39203-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39203-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39203-107">DESCRIPTION</span></span>
<span data-ttu-id="39203-108">**AzureRmNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대 한 Azure 네트워크 보안 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39203-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="39203-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39203-109">EXAMPLES</span></span>

### <span data-ttu-id="39203-110">1: RDP를 허용 하는 네트워크 보안 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="39203-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="39203-111">이 명령은 인터넷에서 포트 3389으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39203-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="39203-112">2: HTTP를 허용 하는 네트워크 보안 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="39203-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="39203-113">이 명령은 인터넷에서 포트 80으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39203-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="39203-114">변수</span><span class="sxs-lookup"><span data-stu-id="39203-114">PARAMETERS</span></span>

### <span data-ttu-id="39203-115">-Access</span><span class="sxs-lookup"><span data-stu-id="39203-115">-Access</span></span>
<span data-ttu-id="39203-116">네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="39203-117">이 매개 변수에 허용 되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="39203-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="39203-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39203-118">-DefaultProfile</span></span>
<span data-ttu-id="39203-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39203-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39203-120">-설명</span><span class="sxs-lookup"><span data-stu-id="39203-120">-Description</span></span>
<span data-ttu-id="39203-121">만들려는 네트워크 보안 규칙 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="39203-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="39203-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="39203-123">대상 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="39203-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39203-125">클래스 없는 도메인간 라우팅 (CIDR) 주소</span><span class="sxs-lookup"><span data-stu-id="39203-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="39203-126">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="39203-126">A destination IP address range</span></span> 
- <span data-ttu-id="39203-127">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="39203-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39203-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="39203-129">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="39203-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="39203-130">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="39203-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="39203-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="39203-132">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="39203-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="39203-133">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="39203-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="39203-134">-DestinationPortRange</span></span>
<span data-ttu-id="39203-135">대상 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="39203-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39203-137">정수</span><span class="sxs-lookup"><span data-stu-id="39203-137">An integer</span></span>
- <span data-ttu-id="39203-138">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="39203-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="39203-139">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="39203-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="39203-140">방향</span><span class="sxs-lookup"><span data-stu-id="39203-140">-Direction</span></span>
<span data-ttu-id="39203-141">들어오는 트래픽이나 보내는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="39203-142">이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="39203-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="39203-143">-이름</span><span class="sxs-lookup"><span data-stu-id="39203-143">-Name</span></span>
<span data-ttu-id="39203-144">이 cmdlet이 만드는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="39203-145">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="39203-145">-Priority</span></span>
<span data-ttu-id="39203-146">규칙 구성의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="39203-147">이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="39203-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="39203-148">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="39203-149">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="39203-150">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="39203-150">-Protocol</span></span>
<span data-ttu-id="39203-151">새 규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="39203-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39203-153">Net.tcp</span><span class="sxs-lookup"><span data-stu-id="39203-153">Tcp</span></span>
- <span data-ttu-id="39203-154">Udp</span><span class="sxs-lookup"><span data-stu-id="39203-154">Udp</span></span>
- <span data-ttu-id="39203-155">와일드 카드 문자 (\*)를 두 개 모두 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="39203-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="39203-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="39203-157">원본 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="39203-158">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39203-159">CIDR</span><span class="sxs-lookup"><span data-stu-id="39203-159">A CIDR</span></span>
- <span data-ttu-id="39203-160">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="39203-160">A source IP range</span></span>
- <span data-ttu-id="39203-161">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="39203-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="39203-162">VirtualNetwork, AzureLoadBalancer 및 Internet 등의 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="39203-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39203-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="39203-164">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="39203-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="39203-165">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="39203-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="39203-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="39203-167">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="39203-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="39203-168">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="39203-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="39203-169">-SourcePortRange</span></span>
<span data-ttu-id="39203-170">원본 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-170">Specifies the source port or range.</span></span>
<span data-ttu-id="39203-171">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39203-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39203-172">정수</span><span class="sxs-lookup"><span data-stu-id="39203-172">An integer</span></span>
- <span data-ttu-id="39203-173">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="39203-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="39203-174">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="39203-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="39203-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39203-175">CommonParameters</span></span>
<span data-ttu-id="39203-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39203-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39203-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39203-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39203-178">입력</span><span class="sxs-lookup"><span data-stu-id="39203-178">INPUTS</span></span>

### <span data-ttu-id="39203-179">않아야</span><span class="sxs-lookup"><span data-stu-id="39203-179">None</span></span>

## <span data-ttu-id="39203-180">출력</span><span class="sxs-lookup"><span data-stu-id="39203-180">OUTPUTS</span></span>

### <span data-ttu-id="39203-181">Microsoft. 네트워크 모델. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="39203-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="39203-182">상속자</span><span class="sxs-lookup"><span data-stu-id="39203-182">NOTES</span></span>

## <span data-ttu-id="39203-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39203-183">RELATED LINKS</span></span>

[<span data-ttu-id="39203-184">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39203-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="39203-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39203-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="39203-186">제거-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39203-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="39203-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39203-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


