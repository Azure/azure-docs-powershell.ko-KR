---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214848"
---
# <span data-ttu-id="da782-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="da782-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="da782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da782-102">SYNOPSIS</span></span>
<span data-ttu-id="da782-103">방화벽 NAT 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da782-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="da782-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da782-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da782-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da782-105">DESCRIPTION</span></span>
<span data-ttu-id="da782-106">**AzFirewallNatRuleCollection** Cmdlet은 방화벽 NAT 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da782-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="da782-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da782-107">EXAMPLES</span></span>

### <span data-ttu-id="da782-108">예제 1: 하나의 규칙을 사용 하 여 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="da782-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="da782-109">이 예제에서는 하나의 규칙이 있는 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="da782-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="da782-110">$Rule 1에서 식별 된 조건과 일치 하는 모든 트래픽은 번역 된 주소 및 포트에 DNAT'ed 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da782-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="da782-111">예제 2: 규칙 컬렉션에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="da782-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="da782-112">이 예제에서는 규칙 하나가 포함 된 새 NAT 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에 메서드 AddRule을 사용 하 여 규칙 컬렉션에 두 번째 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="da782-113">지정 된 규칙 컬렉션의 각 규칙 이름은 고유한 이름을 가져야 하 고 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="da782-114">예제 3: 규칙 컬렉션에서 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="da782-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="da782-115">이 예제에서는 규칙 하나가 포함 된 새 NAT 규칙 컬렉션을 만든 다음 이름으로 규칙을 가져오고, 규칙 컬렉션 개체에서 GetRuleByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="da782-116">메서드 GetRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="da782-117">예제 4: 규칙 컬렉션에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="da782-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="da782-118">이 예제에서는 두 개의 규칙이 있는 새 NAT 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체의 메서드 RemoveRuleByName를 호출 하 여 규칙 컬렉션에서 첫 번째 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="da782-119">메서드 RemoveRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="da782-120">변수</span><span class="sxs-lookup"><span data-stu-id="da782-120">PARAMETERS</span></span>

### <span data-ttu-id="da782-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da782-121">-DefaultProfile</span></span>
<span data-ttu-id="da782-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da782-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da782-123">-이름</span><span class="sxs-lookup"><span data-stu-id="da782-123">-Name</span></span>
<span data-ttu-id="da782-124">이 NAT 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="da782-125">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="da782-126">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="da782-126">-Priority</span></span>
<span data-ttu-id="da782-127">이 규칙의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="da782-128">Priority는 100과 65000 사이의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="da782-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="da782-129">숫자가 작을수록 우선 순위가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="da782-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="da782-130">-규칙</span><span class="sxs-lookup"><span data-stu-id="da782-130">-Rule</span></span>
<span data-ttu-id="da782-131">이 컬렉션 아래에서 그룹화 할 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="da782-132">-확인</span><span class="sxs-lookup"><span data-stu-id="da782-132">-Confirm</span></span>
<span data-ttu-id="da782-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da782-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da782-134">-WhatIf</span></span>
<span data-ttu-id="da782-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da782-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da782-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da782-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da782-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da782-137">CommonParameters</span></span>
<span data-ttu-id="da782-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da782-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da782-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da782-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da782-140">입력</span><span class="sxs-lookup"><span data-stu-id="da782-140">INPUTS</span></span>

### <span data-ttu-id="da782-141">않아야</span><span class="sxs-lookup"><span data-stu-id="da782-141">None</span></span>

## <span data-ttu-id="da782-142">출력</span><span class="sxs-lookup"><span data-stu-id="da782-142">OUTPUTS</span></span>

### <span data-ttu-id="da782-143">PSAzureFirewallNatRuleCollection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="da782-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="da782-144">상속자</span><span class="sxs-lookup"><span data-stu-id="da782-144">NOTES</span></span>

## <span data-ttu-id="da782-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da782-145">RELATED LINKS</span></span>

[<span data-ttu-id="da782-146">새로운 AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="da782-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="da782-147">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="da782-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="da782-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="da782-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
