---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 34397a467cb25a6b93963f8944096975663ccf5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881829"
---
# <span data-ttu-id="9c682-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c682-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9c682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c682-102">SYNOPSIS</span></span>
<span data-ttu-id="9c682-103">네트워크 보안 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c682-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c682-104">SYNTAX</span></span>

### <span data-ttu-id="9c682-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="9c682-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="9c682-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c682-106">SetByResourceId</span></span>
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

## <span data-ttu-id="9c682-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9c682-107">DESCRIPTION</span></span>
<span data-ttu-id="9c682-108">**AzureRmNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대 한 Azure 네트워크 보안 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="9c682-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9c682-109">EXAMPLES</span></span>

### <span data-ttu-id="9c682-110">1: RDP를 허용 하는 네트워크 보안 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="9c682-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="9c682-111">이 명령은 인터넷에서 포트 3389으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="9c682-112">2: HTTP를 허용 하는 네트워크 보안 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="9c682-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="9c682-113">이 명령은 인터넷에서 포트 80으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="9c682-114">변수</span><span class="sxs-lookup"><span data-stu-id="9c682-114">PARAMETERS</span></span>

### <span data-ttu-id="9c682-115">-Access</span><span class="sxs-lookup"><span data-stu-id="9c682-115">-Access</span></span>
<span data-ttu-id="9c682-116">네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="9c682-117">이 매개 변수에 허용 되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="9c682-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c682-118">-DefaultProfile</span></span>
<span data-ttu-id="9c682-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c682-120">-설명</span><span class="sxs-lookup"><span data-stu-id="9c682-120">-Description</span></span>
<span data-ttu-id="9c682-121">만들려는 네트워크 보안 규칙 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="9c682-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9c682-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="9c682-123">대상 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="9c682-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c682-125">클래스 없는 도메인간 라우팅 (CIDR) 주소</span><span class="sxs-lookup"><span data-stu-id="9c682-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="9c682-126">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="9c682-126">A destination IP address range</span></span> 
- <span data-ttu-id="9c682-127">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="9c682-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="9c682-128">VirtualNetwork, AzureLoadBalancer, 인터넷 등의 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="9c682-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9c682-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="9c682-130">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="9c682-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9c682-131">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9c682-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9c682-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="9c682-133">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="9c682-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9c682-134">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9c682-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="9c682-135">-DestinationPortRange</span></span>
<span data-ttu-id="9c682-136">대상 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="9c682-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c682-138">정수</span><span class="sxs-lookup"><span data-stu-id="9c682-138">An integer</span></span>
- <span data-ttu-id="9c682-139">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="9c682-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9c682-140">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="9c682-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9c682-141">방향</span><span class="sxs-lookup"><span data-stu-id="9c682-141">-Direction</span></span>
<span data-ttu-id="9c682-142">들어오는 트래픽이나 보내는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="9c682-143">이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="9c682-144">-이름</span><span class="sxs-lookup"><span data-stu-id="9c682-144">-Name</span></span>
<span data-ttu-id="9c682-145">이 cmdlet이 만드는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9c682-146">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="9c682-146">-Priority</span></span>
<span data-ttu-id="9c682-147">규칙 구성의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="9c682-148">이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="9c682-149">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="9c682-150">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="9c682-151">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="9c682-151">-Protocol</span></span>
<span data-ttu-id="9c682-152">새 규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="9c682-153">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c682-154">Net.tcp</span><span class="sxs-lookup"><span data-stu-id="9c682-154">Tcp</span></span>
- <span data-ttu-id="9c682-155">Udp</span><span class="sxs-lookup"><span data-stu-id="9c682-155">Udp</span></span>
- <span data-ttu-id="9c682-156">와일드 카드 문자 (\*)를 두 개 모두 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="9c682-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9c682-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="9c682-158">원본 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="9c682-159">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c682-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="9c682-160">A CIDR</span></span>
- <span data-ttu-id="9c682-161">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="9c682-161">A source IP range</span></span>
- <span data-ttu-id="9c682-162">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)입니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="9c682-163">VirtualNetwork, AzureLoadBalancer 및 Internet 등의 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="9c682-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9c682-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="9c682-165">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="9c682-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="9c682-166">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9c682-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9c682-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="9c682-168">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="9c682-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="9c682-169">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9c682-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="9c682-170">-SourcePortRange</span></span>
<span data-ttu-id="9c682-171">원본 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-171">Specifies the source port or range.</span></span>
<span data-ttu-id="9c682-172">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c682-173">정수</span><span class="sxs-lookup"><span data-stu-id="9c682-173">An integer</span></span>
- <span data-ttu-id="9c682-174">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="9c682-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9c682-175">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="9c682-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9c682-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c682-176">CommonParameters</span></span>
<span data-ttu-id="9c682-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c682-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c682-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c682-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c682-179">입력</span><span class="sxs-lookup"><span data-stu-id="9c682-179">INPUTS</span></span>

## <span data-ttu-id="9c682-180">출력</span><span class="sxs-lookup"><span data-stu-id="9c682-180">OUTPUTS</span></span>

### <span data-ttu-id="9c682-181">Microsoft. 네트워크 모델. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9c682-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="9c682-182">상속자</span><span class="sxs-lookup"><span data-stu-id="9c682-182">NOTES</span></span>

## <span data-ttu-id="9c682-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c682-183">RELATED LINKS</span></span>

[<span data-ttu-id="9c682-184">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c682-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9c682-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c682-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9c682-186">제거-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c682-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9c682-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c682-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


