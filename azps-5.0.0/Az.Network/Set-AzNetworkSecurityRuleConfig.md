---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216736"
---
# <span data-ttu-id="1ee4e-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee4e-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="1ee4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ee4e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee4e-103">네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="1ee4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ee4e-104">SYNTAX</span></span>

### <span data-ttu-id="1ee4e-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ee4e-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ee4e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ee4e-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ee4e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1ee4e-107">DESCRIPTION</span></span>
<span data-ttu-id="1ee4e-108">**Set-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="1ee4e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1ee4e-109">EXAMPLES</span></span>

### <span data-ttu-id="1ee4e-110">예제 1: 네트워크 보안 규칙에서 access 구성 변경</span><span class="sxs-lookup"><span data-stu-id="1ee4e-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="1ee4e-111">첫 번째 명령은 NSG-프런트 엔드 라는 네트워크 보안 그룹을 가져온 다음 변수 $nsg에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="1ee4e-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $nsg의 보안 그룹을 Get-AzNetworkSecurityRuleConfig에 전달 하 고,이는 rdp-rule 라는 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="1ee4e-113">세 번째 명령은 rdp 규칙의 액세스 구성을 Deny로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="1ee4e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="1ee4e-114">Example 2</span></span>

<span data-ttu-id="1ee4e-115">네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="1ee4e-116">생성</span><span class="sxs-lookup"><span data-stu-id="1ee4e-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="1ee4e-117">변수</span><span class="sxs-lookup"><span data-stu-id="1ee4e-117">PARAMETERS</span></span>

### <span data-ttu-id="1ee4e-118">-Access</span><span class="sxs-lookup"><span data-stu-id="1ee4e-118">-Access</span></span>
<span data-ttu-id="1ee4e-119">네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="1ee4e-120">이 매개 변수에 허용 되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="1ee4e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee4e-121">-DefaultProfile</span></span>
<span data-ttu-id="1ee4e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee4e-123">-설명</span><span class="sxs-lookup"><span data-stu-id="1ee4e-123">-Description</span></span>
<span data-ttu-id="1ee4e-124">규칙 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="1ee4e-125">최대 크기는 140 자입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="1ee4e-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ee4e-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="1ee4e-127">대상 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="1ee4e-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ee4e-129">클래스 없는 도메인간 라우팅 (CIDR) 주소</span><span class="sxs-lookup"><span data-stu-id="1ee4e-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="1ee4e-130">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="1ee4e-130">A destination IP address range</span></span> 
- <span data-ttu-id="1ee4e-131">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="1ee4e-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee4e-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="1ee4e-133">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="1ee4e-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1ee4e-134">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1ee4e-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1ee4e-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="1ee4e-136">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="1ee4e-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1ee4e-137">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1ee4e-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="1ee4e-138">-DestinationPortRange</span></span>
<span data-ttu-id="1ee4e-139">대상 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="1ee4e-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ee4e-141">정수</span><span class="sxs-lookup"><span data-stu-id="1ee4e-141">An integer</span></span> 
- <span data-ttu-id="1ee4e-142">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="1ee4e-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1ee4e-143">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="1ee4e-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="1ee4e-144">방향</span><span class="sxs-lookup"><span data-stu-id="1ee4e-144">-Direction</span></span>
<span data-ttu-id="1ee4e-145">들어오는 트래픽 또는 나가는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="1ee4e-146">이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="1ee4e-147">-이름</span><span class="sxs-lookup"><span data-stu-id="1ee4e-147">-Name</span></span>
<span data-ttu-id="1ee4e-148">이 cmdlet이 설정 하는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1ee4e-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee4e-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1ee4e-150">설정할 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="1ee4e-151">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="1ee4e-151">-Priority</span></span>
<span data-ttu-id="1ee4e-152">규칙 구성의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="1ee4e-153">이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="1ee4e-154">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="1ee4e-155">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="1ee4e-156">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="1ee4e-156">-Protocol</span></span>
<span data-ttu-id="1ee4e-157">규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="1ee4e-158">이 매개 변수에 허용 되는 값은:--Tcp</span><span class="sxs-lookup"><span data-stu-id="1ee4e-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="1ee4e-159">Udp</span><span class="sxs-lookup"><span data-stu-id="1ee4e-159">Udp</span></span>
- <span data-ttu-id="1ee4e-160">둘 다 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="1ee4e-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="1ee4e-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ee4e-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="1ee4e-162">원본 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="1ee4e-163">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ee4e-164">CIDR</span><span class="sxs-lookup"><span data-stu-id="1ee4e-164">A CIDR</span></span>
- <span data-ttu-id="1ee4e-165">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="1ee4e-165">A source IP range</span></span>
- <span data-ttu-id="1ee4e-166">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그도 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="1ee4e-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee4e-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="1ee4e-168">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="1ee4e-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="1ee4e-169">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1ee4e-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1ee4e-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="1ee4e-171">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="1ee4e-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="1ee4e-172">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1ee4e-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="1ee4e-173">-SourcePortRange</span></span>
<span data-ttu-id="1ee4e-174">원본 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-174">Specifies the source port or range.</span></span>
<span data-ttu-id="1ee4e-175">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ee4e-176">정수</span><span class="sxs-lookup"><span data-stu-id="1ee4e-176">An integer</span></span>
- <span data-ttu-id="1ee4e-177">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="1ee4e-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1ee4e-178">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="1ee4e-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="1ee4e-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee4e-179">CommonParameters</span></span>
<span data-ttu-id="1ee4e-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee4e-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee4e-181">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee4e-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee4e-182">입력</span><span class="sxs-lookup"><span data-stu-id="1ee4e-182">INPUTS</span></span>

### <span data-ttu-id="1ee4e-183">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee4e-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1ee4e-184">출력</span><span class="sxs-lookup"><span data-stu-id="1ee4e-184">OUTPUTS</span></span>

### <span data-ttu-id="1ee4e-185">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ee4e-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1ee4e-186">상속자</span><span class="sxs-lookup"><span data-stu-id="1ee4e-186">NOTES</span></span>

## <span data-ttu-id="1ee4e-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ee4e-187">RELATED LINKS</span></span>

[<span data-ttu-id="1ee4e-188">추가-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee4e-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1ee4e-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee4e-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1ee4e-190">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee4e-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1ee4e-191">제거-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1ee4e-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


