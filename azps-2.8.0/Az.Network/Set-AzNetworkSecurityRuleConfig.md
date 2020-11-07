---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869533"
---
# <span data-ttu-id="42038-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42038-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="42038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42038-102">SYNOPSIS</span></span>
<span data-ttu-id="42038-103">네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="42038-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42038-104">SYNTAX</span></span>

### <span data-ttu-id="42038-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="42038-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42038-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="42038-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42038-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42038-107">DESCRIPTION</span></span>
<span data-ttu-id="42038-108">**Set-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="42038-109">예제의</span><span class="sxs-lookup"><span data-stu-id="42038-109">EXAMPLES</span></span>

### <span data-ttu-id="42038-110">예제 1: 네트워크 보안 규칙에서 access 구성 변경</span><span class="sxs-lookup"><span data-stu-id="42038-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="42038-111">첫 번째 명령은 NSG-프런트 엔드 라는 네트워크 보안 그룹을 가져온 다음 변수 $nsg에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="42038-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $nsg의 보안 그룹을 Get-AzNetworkSecurityRuleConfig에 전달 하 고,이는 rdp-rule 라는 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42038-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="42038-113">세 번째 명령은 rdp 규칙의 액세스 구성을 Deny로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="42038-114">변수</span><span class="sxs-lookup"><span data-stu-id="42038-114">PARAMETERS</span></span>

### <span data-ttu-id="42038-115">-Access</span><span class="sxs-lookup"><span data-stu-id="42038-115">-Access</span></span>
<span data-ttu-id="42038-116">네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="42038-117">이 매개 변수에 허용 되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="42038-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="42038-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42038-118">-DefaultProfile</span></span>
<span data-ttu-id="42038-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42038-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42038-120">-설명</span><span class="sxs-lookup"><span data-stu-id="42038-120">-Description</span></span>
<span data-ttu-id="42038-121">규칙 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="42038-122">최대 크기는 140 자입니다.</span><span class="sxs-lookup"><span data-stu-id="42038-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="42038-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="42038-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="42038-124">대상 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="42038-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42038-126">클래스 없는 도메인간 라우팅 (CIDR) 주소</span><span class="sxs-lookup"><span data-stu-id="42038-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="42038-127">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="42038-127">A destination IP address range</span></span> 
- <span data-ttu-id="42038-128">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="42038-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="42038-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="42038-130">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="42038-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="42038-131">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="42038-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="42038-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="42038-133">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="42038-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="42038-134">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="42038-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="42038-135">-DestinationPortRange</span></span>
<span data-ttu-id="42038-136">대상 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="42038-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42038-138">정수</span><span class="sxs-lookup"><span data-stu-id="42038-138">An integer</span></span> 
- <span data-ttu-id="42038-139">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="42038-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="42038-140">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="42038-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="42038-141">방향</span><span class="sxs-lookup"><span data-stu-id="42038-141">-Direction</span></span>
<span data-ttu-id="42038-142">들어오는 트래픽 또는 나가는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="42038-143">이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="42038-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="42038-144">-이름</span><span class="sxs-lookup"><span data-stu-id="42038-144">-Name</span></span>
<span data-ttu-id="42038-145">이 cmdlet이 설정 하는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="42038-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="42038-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="42038-147">설정할 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="42038-148">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="42038-148">-Priority</span></span>
<span data-ttu-id="42038-149">규칙 구성의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="42038-150">이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="42038-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="42038-151">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="42038-152">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="42038-153">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="42038-153">-Protocol</span></span>
<span data-ttu-id="42038-154">규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="42038-155">이 매개 변수에 허용 되는 값은:--Tcp</span><span class="sxs-lookup"><span data-stu-id="42038-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="42038-156">Udp</span><span class="sxs-lookup"><span data-stu-id="42038-156">Udp</span></span>
- <span data-ttu-id="42038-157">둘 다 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="42038-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="42038-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="42038-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="42038-159">원본 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="42038-160">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42038-161">CIDR</span><span class="sxs-lookup"><span data-stu-id="42038-161">A CIDR</span></span>
- <span data-ttu-id="42038-162">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="42038-162">A source IP range</span></span>
- <span data-ttu-id="42038-163">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그도 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="42038-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="42038-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="42038-165">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="42038-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="42038-166">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="42038-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="42038-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="42038-168">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="42038-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="42038-169">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="42038-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="42038-170">-SourcePortRange</span></span>
<span data-ttu-id="42038-171">원본 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-171">Specifies the source port or range.</span></span>
<span data-ttu-id="42038-172">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42038-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42038-173">정수</span><span class="sxs-lookup"><span data-stu-id="42038-173">An integer</span></span>
- <span data-ttu-id="42038-174">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="42038-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="42038-175">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="42038-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="42038-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42038-176">CommonParameters</span></span>
<span data-ttu-id="42038-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42038-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42038-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42038-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42038-179">입력</span><span class="sxs-lookup"><span data-stu-id="42038-179">INPUTS</span></span>

### <span data-ttu-id="42038-180">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="42038-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="42038-181">출력</span><span class="sxs-lookup"><span data-stu-id="42038-181">OUTPUTS</span></span>

### <span data-ttu-id="42038-182">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="42038-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="42038-183">상속자</span><span class="sxs-lookup"><span data-stu-id="42038-183">NOTES</span></span>

## <span data-ttu-id="42038-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42038-184">RELATED LINKS</span></span>

[<span data-ttu-id="42038-185">추가-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42038-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="42038-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42038-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="42038-187">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42038-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="42038-188">제거-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="42038-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


