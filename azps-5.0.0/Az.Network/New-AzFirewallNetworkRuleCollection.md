---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309582"
---
# <span data-ttu-id="b1b91-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b1b91-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="b1b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b91-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b91-103">네트워크 규칙의 Azure 방화벽 네트워크 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="b1b91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1b91-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b91-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1b91-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b91-106">**AzFirewallNetworkRuleCollection** Cmdlet은 방화벽 네트워크 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="b1b91-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1b91-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b91-108">예제 1: 두 가지 규칙을 사용 하 여 네트워크 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="b1b91-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="b1b91-109">이 예제에서는 두 규칙 중 하 나와 일치 하는 모든 트래픽을 허용 하는 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="b1b91-110">첫 번째 규칙은 모든 UDP 트래픽에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="b1b91-111">두 번째 규칙은 10.0.0.0에서 60.1.5.0:4040 TCP 트래픽에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="b1b91-112">$Rule 1 또는 $rule 2에서 식별 된 트래픽에만 일치 하는 더 높은 우선 순위의 네트워크 규칙 컬렉션이 있는 경우에는 우선 순위가 높은 규칙 모음의 작업이 대신 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="b1b91-113">예제 2: 규칙 컬렉션에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="b1b91-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="b1b91-114">이 예제에서는 규칙 하나가 포함 된 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에 메서드 AddRule을 사용 하 여 규칙 컬렉션에 두 번째 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="b1b91-115">지정 된 규칙 컬렉션의 각 규칙 이름은 고유한 이름을 가져야 하 고 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="b1b91-116">예제 3: 규칙 컬렉션에서 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1b91-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="b1b91-117">이 예제에서는 규칙 하나가 포함 된 새 네트워크 규칙 컬렉션을 만든 다음, 규칙 컬렉션 개체의 GetRuleByName 메서드를 호출 하 여 이름을 기준으로 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="b1b91-118">메서드 GetRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="b1b91-119">예제 4: 규칙 컬렉션에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="b1b91-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="b1b91-120">이 예제에서는 두 개의 규칙이 있는 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체의 메서드 RemoveRuleByName를 호출 하 여 규칙 컬렉션에서 첫 번째 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="b1b91-121">메서드 RemoveRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="b1b91-122">변수</span><span class="sxs-lookup"><span data-stu-id="b1b91-122">PARAMETERS</span></span>

### <span data-ttu-id="b1b91-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="b1b91-123">-ActionType</span></span>
<span data-ttu-id="b1b91-124">이 규칙의 트래픽 일치 조건에 대해 수행할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="b1b91-125">허용 되는 작업은 "허용" 또는 "거부"입니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="b1b91-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b91-126">-DefaultProfile</span></span>
<span data-ttu-id="b1b91-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b91-128">-이름</span><span class="sxs-lookup"><span data-stu-id="b1b91-128">-Name</span></span>
<span data-ttu-id="b1b91-129">이 네트워크 규칙 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="b1b91-130">이름은 모든 네트워크 규칙 모음에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="b1b91-131">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="b1b91-131">-Priority</span></span>
<span data-ttu-id="b1b91-132">이 규칙 컬렉션의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="b1b91-133">Priority는 100과 65000 사이의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="b1b91-134">숫자가 작을수록 우선 순위가 높습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="b1b91-135">-규칙</span><span class="sxs-lookup"><span data-stu-id="b1b91-135">-Rule</span></span>
<span data-ttu-id="b1b91-136">이 컬렉션 아래에서 그룹화 할 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="b1b91-137">-확인</span><span class="sxs-lookup"><span data-stu-id="b1b91-137">-Confirm</span></span>
<span data-ttu-id="b1b91-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b91-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b91-139">-WhatIf</span></span>
<span data-ttu-id="b1b91-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b91-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b91-142">CommonParameters</span></span>
<span data-ttu-id="b1b91-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1b91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b91-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b91-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b91-145">입력</span><span class="sxs-lookup"><span data-stu-id="b1b91-145">INPUTS</span></span>

### <span data-ttu-id="b1b91-146">않아야</span><span class="sxs-lookup"><span data-stu-id="b1b91-146">None</span></span>

## <span data-ttu-id="b1b91-147">출력</span><span class="sxs-lookup"><span data-stu-id="b1b91-147">OUTPUTS</span></span>

### <span data-ttu-id="b1b91-148">PSAzureFirewallNetworkRuleCollection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b1b91-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="b1b91-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b1b91-149">NOTES</span></span>

## <span data-ttu-id="b1b91-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1b91-150">RELATED LINKS</span></span>

[<span data-ttu-id="b1b91-151">새로운 AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b1b91-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="b1b91-152">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1b91-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b1b91-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b1b91-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
