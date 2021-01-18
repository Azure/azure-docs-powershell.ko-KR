---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492619"
---
# <span data-ttu-id="997fc-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="997fc-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="997fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="997fc-102">SYNOPSIS</span></span>
<span data-ttu-id="997fc-103">네트워크 규칙의 Azure Firewall 네트워크 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="997fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="997fc-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="997fc-105">설명</span><span class="sxs-lookup"><span data-stu-id="997fc-105">DESCRIPTION</span></span>
<span data-ttu-id="997fc-106">**New-AzFirewallNetworkRuleCollection** cmdlet은 방화벽 네트워크 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="997fc-107">예제</span><span class="sxs-lookup"><span data-stu-id="997fc-107">EXAMPLES</span></span>

### <span data-ttu-id="997fc-108">예제 1: 두 개의 규칙이 있는 네트워크 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="997fc-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="997fc-109">이 예제에서는 두 규칙 중 하나와 일치하는 모든 트래픽을 허용하는 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="997fc-110">첫 번째 규칙은 모든 UDP 트래픽에 대한 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="997fc-111">두 번째 규칙은 10.0.0.0에서 60.1.5.0:4040까지의 TCP 트래픽에 대한 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="997fc-112">$rule 1 또는 $rule 2에서 식별된 트래픽과 일치하는 우선 순위가 더 높은 다른 네트워크 규칙 컬렉션이 있는 경우 우선 순위가 더 높은 규칙 컬렉션의 작업이 대신 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="997fc-113">예제 2: 규칙 컬렉션에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="997fc-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="997fc-114">이 예제에서는 하나의 규칙으로 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 AddRule 메서드를 사용하여 규칙 컬렉션에 두 번째 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="997fc-115">지정한 규칙 컬렉션의 각 규칙 이름에는 고유한 이름이 있어야 합니다. 대소문자는 대소문자 고유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="997fc-116">예제 3: 규칙 컬렉션에서 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="997fc-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="997fc-117">이 예제에서는 하나의 규칙으로 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 GetRuleByName 메서드를 호출하여 이름으로 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="997fc-118">GetRuleByName 메서드의 규칙 이름은 대소문자 비대칭입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="997fc-119">예제 4: 규칙 컬렉션에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="997fc-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="997fc-120">이 예제에서는 두 개의 규칙으로 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 RemoveRuleByName 메서드를 호출하여 규칙 컬렉션에서 첫 번째 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="997fc-121">RemoveRuleByName 메서드의 규칙 이름은 대소문자 불일치입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="997fc-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="997fc-122">PARAMETERS</span></span>

### <span data-ttu-id="997fc-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="997fc-123">-ActionType</span></span>
<span data-ttu-id="997fc-124">이 규칙의 트래픽 일치 조건에 대해 수행될 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="997fc-125">허용되는 작업은 "허용" 또는 "거부"입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997fc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="997fc-126">-DefaultProfile</span></span>
<span data-ttu-id="997fc-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="997fc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="997fc-128">-Name</span></span>
<span data-ttu-id="997fc-129">이 네트워크 규칙 컬렉션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="997fc-130">이름은 모든 네트워크 규칙 컬렉션에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="997fc-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="997fc-131">-Priority</span></span>
<span data-ttu-id="997fc-132">이 규칙 컬렉션의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="997fc-133">우선 순위는 100에서 65000 사이의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="997fc-134">숫자가 작을수록 우선 순위가 높아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997fc-135">-Rule</span><span class="sxs-lookup"><span data-stu-id="997fc-135">-Rule</span></span>
<span data-ttu-id="997fc-136">이 컬렉션에서 그룹화할 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997fc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="997fc-137">-Confirm</span></span>
<span data-ttu-id="997fc-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997fc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="997fc-139">-WhatIf</span></span>
<span data-ttu-id="997fc-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="997fc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="997fc-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997fc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="997fc-142">CommonParameters</span></span>
<span data-ttu-id="997fc-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="997fc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="997fc-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="997fc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="997fc-145">입력</span><span class="sxs-lookup"><span data-stu-id="997fc-145">INPUTS</span></span>

### <span data-ttu-id="997fc-146">없음</span><span class="sxs-lookup"><span data-stu-id="997fc-146">None</span></span>

## <span data-ttu-id="997fc-147">출력</span><span class="sxs-lookup"><span data-stu-id="997fc-147">OUTPUTS</span></span>

### <span data-ttu-id="997fc-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="997fc-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="997fc-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="997fc-149">NOTES</span></span>

## <span data-ttu-id="997fc-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="997fc-150">RELATED LINKS</span></span>

[<span data-ttu-id="997fc-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="997fc-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="997fc-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="997fc-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="997fc-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="997fc-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
