---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 8a1e4cb97f151843f92697a2a230bd2721a56f29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882169"
---
# <span data-ttu-id="2f2e7-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f2e7-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="2f2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2e7-103">네트워크 보안 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f2e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f2e7-104">SYNTAX</span></span>

### <span data-ttu-id="2f2e7-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="2f2e7-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="2f2e7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f2e7-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f2e7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2f2e7-107">DESCRIPTION</span></span>
<span data-ttu-id="2f2e7-108">**AzureRmNetworkSecurityRuleConfig** Cmdlet은 Azure 네트워크 보안 규칙 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="2f2e7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2f2e7-109">EXAMPLES</span></span>

### <span data-ttu-id="2f2e7-110">예제 1: 네트워크 보안 규칙에서 access 구성 변경</span><span class="sxs-lookup"><span data-stu-id="2f2e7-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="2f2e7-111">첫 번째 명령은 NSG-프런트 엔드 라는 네트워크 보안 그룹을 가져온 다음 변수 $nsg에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="2f2e7-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $nsg의 보안 그룹을 Get-AzureRmNetworkSecurityRuleConfig에 전달 하 고,이는 rdp-rule 라는 보안 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="2f2e7-113">세 번째 명령은 rdp 규칙의 액세스 구성을 Deny로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="2f2e7-114">변수</span><span class="sxs-lookup"><span data-stu-id="2f2e7-114">PARAMETERS</span></span>

### <span data-ttu-id="2f2e7-115">-Access</span><span class="sxs-lookup"><span data-stu-id="2f2e7-115">-Access</span></span>
<span data-ttu-id="2f2e7-116">네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="2f2e7-117">이 매개 변수에 허용 되는 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="2f2e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2e7-118">-DefaultProfile</span></span>
<span data-ttu-id="2f2e7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f2e7-120">-설명</span><span class="sxs-lookup"><span data-stu-id="2f2e7-120">-Description</span></span>
<span data-ttu-id="2f2e7-121">규칙 구성에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="2f2e7-122">최대 크기는 140 자입니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="2f2e7-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2f2e7-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="2f2e7-124">대상 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="2f2e7-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f2e7-126">클래스 없는 도메인간 라우팅 (CIDR) 주소</span><span class="sxs-lookup"><span data-stu-id="2f2e7-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="2f2e7-127">대상 IP 주소 범위</span><span class="sxs-lookup"><span data-stu-id="2f2e7-127">A destination IP address range</span></span> 
- <span data-ttu-id="2f2e7-128">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="2f2e7-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="2f2e7-129">VirtualNetwork, AzureLoadBalancer, 인터넷 등의 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="2f2e7-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f2e7-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="2f2e7-131">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="2f2e7-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="2f2e7-132">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2f2e7-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2f2e7-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="2f2e7-134">규칙의 대상으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="2f2e7-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="2f2e7-135">' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2f2e7-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="2f2e7-136">-DestinationPortRange</span></span>
<span data-ttu-id="2f2e7-137">대상 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="2f2e7-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f2e7-139">정수</span><span class="sxs-lookup"><span data-stu-id="2f2e7-139">An integer</span></span> 
- <span data-ttu-id="2f2e7-140">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="2f2e7-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="2f2e7-141">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="2f2e7-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="2f2e7-142">방향</span><span class="sxs-lookup"><span data-stu-id="2f2e7-142">-Direction</span></span>
<span data-ttu-id="2f2e7-143">들어오는 트래픽 또는 나가는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="2f2e7-144">이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="2f2e7-145">-이름</span><span class="sxs-lookup"><span data-stu-id="2f2e7-145">-Name</span></span>
<span data-ttu-id="2f2e7-146">이 cmdlet이 설정 하는 네트워크 보안 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2f2e7-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f2e7-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2f2e7-148">설정할 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="2f2e7-149">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="2f2e7-149">-Priority</span></span>
<span data-ttu-id="2f2e7-150">규칙 구성의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="2f2e7-151">이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="2f2e7-152">우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="2f2e7-153">우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="2f2e7-154">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="2f2e7-154">-Protocol</span></span>
<span data-ttu-id="2f2e7-155">규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="2f2e7-156">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="2f2e7-157">--Tcp</span><span class="sxs-lookup"><span data-stu-id="2f2e7-157">--Tcp</span></span>
- <span data-ttu-id="2f2e7-158">Udp</span><span class="sxs-lookup"><span data-stu-id="2f2e7-158">Udp</span></span>
- <span data-ttu-id="2f2e7-159">둘 다 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="2f2e7-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="2f2e7-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2f2e7-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="2f2e7-161">원본 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="2f2e7-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f2e7-163">CIDR</span><span class="sxs-lookup"><span data-stu-id="2f2e7-163">A CIDR</span></span>
- <span data-ttu-id="2f2e7-164">원본 IP 범위</span><span class="sxs-lookup"><span data-stu-id="2f2e7-164">A source IP range</span></span>
- <span data-ttu-id="2f2e7-165">모든 IP 주소와 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="2f2e7-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="2f2e7-166">VirtualNetwork, AzureLoadBalancer 및 Internet 등의 태그를 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="2f2e7-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f2e7-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="2f2e7-168">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="2f2e7-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="2f2e7-169">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2f2e7-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2f2e7-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="2f2e7-171">규칙의 원본으로 설정 된 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="2f2e7-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="2f2e7-172">' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2f2e7-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="2f2e7-173">-SourcePortRange</span></span>
<span data-ttu-id="2f2e7-174">원본 포트 또는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-174">Specifies the source port or range.</span></span>
<span data-ttu-id="2f2e7-175">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f2e7-176">정수</span><span class="sxs-lookup"><span data-stu-id="2f2e7-176">An integer</span></span>
- <span data-ttu-id="2f2e7-177">0에서 65535 사이의 정수 범위</span><span class="sxs-lookup"><span data-stu-id="2f2e7-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="2f2e7-178">모든 포트에 일치 하는 와일드 카드 문자 (\*)</span><span class="sxs-lookup"><span data-stu-id="2f2e7-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="2f2e7-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2e7-179">CommonParameters</span></span>
<span data-ttu-id="2f2e7-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2e7-181">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f2e7-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2e7-182">입력</span><span class="sxs-lookup"><span data-stu-id="2f2e7-182">INPUTS</span></span>

### <span data-ttu-id="2f2e7-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f2e7-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="2f2e7-184">' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f2e7-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="2f2e7-185">출력</span><span class="sxs-lookup"><span data-stu-id="2f2e7-185">OUTPUTS</span></span>

### <span data-ttu-id="2f2e7-186">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2f2e7-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="2f2e7-187">상속자</span><span class="sxs-lookup"><span data-stu-id="2f2e7-187">NOTES</span></span>

## <span data-ttu-id="2f2e7-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f2e7-188">RELATED LINKS</span></span>

[<span data-ttu-id="2f2e7-189">추가-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f2e7-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2f2e7-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f2e7-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2f2e7-191">새로운 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f2e7-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2f2e7-192">제거-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2f2e7-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)


