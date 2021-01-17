---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347678"
---
# <span data-ttu-id="a4807-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a4807-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="a4807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4807-102">SYNOPSIS</span></span>
<span data-ttu-id="a4807-103">방화벽 NAT 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="a4807-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4807-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4807-105">설명</span><span class="sxs-lookup"><span data-stu-id="a4807-105">DESCRIPTION</span></span>
<span data-ttu-id="a4807-106">**New-AzFirewallNatRuleCollection** cmdlet은 방화벽 NAT 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="a4807-107">예제</span><span class="sxs-lookup"><span data-stu-id="a4807-107">EXAMPLES</span></span>

### <span data-ttu-id="a4807-108">예제 1: 하나의 규칙으로 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="a4807-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="a4807-109">이 예제에서는 하나의 규칙으로 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="a4807-110">$rule 1에서 식별된 조건과 일치하는 모든 트래픽은 DNAT에서 변환된 주소 및 포트로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="a4807-111">예제 2: 규칙 컬렉션에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="a4807-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="a4807-112">이 예제에서는 하나의 규칙으로 새 NAT 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 AddRule 메서드를 사용하여 규칙 컬렉션에 두 번째 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="a4807-113">지정한 규칙 컬렉션의 각 규칙 이름은 고유한 이름을 가지고 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="a4807-114">예제 3: 규칙 컬렉션에서 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="a4807-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="a4807-115">이 예제에서는 하나의 규칙으로 새 NAT 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 GetRuleByName 메서드를 호출하여 이름으로 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="a4807-116">GetRuleByName 메서드의 규칙 이름은 대소문자 비대칭입니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="a4807-117">예제 4: 규칙 컬렉션에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="a4807-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="a4807-118">이 예제에서는 두 개의 규칙이 있는 새 NAT 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 RemoveRuleByName 메서드를 호출하여 규칙 컬렉션에서 첫 번째 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="a4807-119">RemoveRuleByName 메서드의 규칙 이름은 대소문자 불일치입니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="a4807-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4807-120">PARAMETERS</span></span>

### <span data-ttu-id="a4807-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4807-121">-DefaultProfile</span></span>
<span data-ttu-id="a4807-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4807-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a4807-123">-Name</span></span>
<span data-ttu-id="a4807-124">이 NAT 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="a4807-125">이름은 규칙 컬렉션 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a4807-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="a4807-126">-Priority</span></span>
<span data-ttu-id="a4807-127">이 규칙의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="a4807-128">우선 순위는 100에서 65000 사이의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="a4807-129">숫자가 작을수록 우선 순위가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="a4807-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="a4807-130">-Rule</span></span>
<span data-ttu-id="a4807-131">이 컬렉션에서 그룹화할 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4807-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4807-132">-Confirm</span></span>
<span data-ttu-id="a4807-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4807-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4807-134">-WhatIf</span></span>
<span data-ttu-id="a4807-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a4807-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4807-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4807-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4807-137">CommonParameters</span></span>
<span data-ttu-id="a4807-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4807-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4807-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4807-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4807-140">입력</span><span class="sxs-lookup"><span data-stu-id="a4807-140">INPUTS</span></span>

### <span data-ttu-id="a4807-141">없음</span><span class="sxs-lookup"><span data-stu-id="a4807-141">None</span></span>

## <span data-ttu-id="a4807-142">출력</span><span class="sxs-lookup"><span data-stu-id="a4807-142">OUTPUTS</span></span>

### <span data-ttu-id="a4807-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a4807-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="a4807-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4807-144">NOTES</span></span>

## <span data-ttu-id="a4807-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4807-145">RELATED LINKS</span></span>

[<span data-ttu-id="a4807-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a4807-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="a4807-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a4807-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a4807-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a4807-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
