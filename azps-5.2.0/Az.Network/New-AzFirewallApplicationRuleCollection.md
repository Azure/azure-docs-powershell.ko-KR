---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367550"
---
# <span data-ttu-id="f2b4d-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f2b4d-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="f2b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b4d-103">방화벽 애플리케이션 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="f2b4d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2b4d-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b4d-105">설명</span><span class="sxs-lookup"><span data-stu-id="f2b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b4d-106">**New-AzFirewallApplicationRuleCollection** cmdlet은 방화벽 애플리케이션 규칙 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="f2b4d-107">예제</span><span class="sxs-lookup"><span data-stu-id="f2b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="f2b4d-108">예제 1: 하나의 규칙으로 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="f2b4d-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="f2b4d-109">이 예제에서는 하나의 규칙으로 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="f2b4d-110">$rule 1에서 식별된 조건과 일치하는 모든 트래픽이 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="f2b4d-111">첫 번째 규칙은 10.0.0.0에서 포트 443의 모든 HTTPS 트래픽에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="f2b4d-112">$rule 1에서 식별된 트래픽과 일치하는 우선 순위가 더 높은 다른 애플리케이션 규칙 컬렉션이 있는 경우 우선 순위가 더 높은 규칙 컬렉션의 작업이 대신 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="f2b4d-113">예제 2: 규칙 컬렉션에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="f2b4d-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="f2b4d-114">이 예제에서는 하나의 규칙으로 새 애플리케이션 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 AddRule 메서드를 사용하여 규칙 컬렉션에 두 번째 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="f2b4d-115">지정한 규칙 컬렉션의 각 규칙 이름에는 고유한 이름이 있어야 합니다. 대소문자는 대소문자 고유하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="f2b4d-116">예제 3: 규칙 컬렉션에서 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="f2b4d-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="f2b4d-117">이 예제에서는 하나의 규칙으로 새 애플리케이션 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 GetRuleByName 메서드를 호출하여 이름으로 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="f2b4d-118">GetRuleByName 메서드의 규칙 이름은 대소문자 비대칭입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="f2b4d-119">예제 4: 규칙 컬렉션에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="f2b4d-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="f2b4d-120">이 예제에서는 두 개의 규칙으로 새 애플리케이션 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 RemoveRuleByName 메서드를 호출하여 규칙 컬렉션에서 첫 번째 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="f2b4d-121">RemoveRuleByName 메서드의 규칙 이름은 대소문자 불일치입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="f2b4d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2b4d-122">PARAMETERS</span></span>

### <span data-ttu-id="f2b4d-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="f2b4d-123">-ActionType</span></span>
<span data-ttu-id="f2b4d-124">규칙 컬렉션의 작업</span><span class="sxs-lookup"><span data-stu-id="f2b4d-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="f2b4d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b4d-125">-DefaultProfile</span></span>
<span data-ttu-id="f2b4d-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b4d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f2b4d-127">-Name</span></span>
<span data-ttu-id="f2b4d-128">이 애플리케이션 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="f2b4d-129">이름은 규칙 컬렉션 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="f2b4d-130">-Priority</span><span class="sxs-lookup"><span data-stu-id="f2b4d-130">-Priority</span></span>
<span data-ttu-id="f2b4d-131">이 규칙의 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="f2b4d-132">우선 순위는 100에서 65000 사이의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="f2b4d-133">숫자가 작을수록 우선 순위가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="f2b4d-134">-Rule</span><span class="sxs-lookup"><span data-stu-id="f2b4d-134">-Rule</span></span>
<span data-ttu-id="f2b4d-135">이 컬렉션에서 그룹화할 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b4d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2b4d-136">-Confirm</span></span>
<span data-ttu-id="f2b4d-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b4d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b4d-138">-WhatIf</span></span>
<span data-ttu-id="f2b4d-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f2b4d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b4d-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b4d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b4d-141">CommonParameters</span></span>
<span data-ttu-id="f2b4d-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b4d-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f2b4d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b4d-144">입력</span><span class="sxs-lookup"><span data-stu-id="f2b4d-144">INPUTS</span></span>

### <span data-ttu-id="f2b4d-145">없음</span><span class="sxs-lookup"><span data-stu-id="f2b4d-145">None</span></span>

## <span data-ttu-id="f2b4d-146">출력</span><span class="sxs-lookup"><span data-stu-id="f2b4d-146">OUTPUTS</span></span>

### <span data-ttu-id="f2b4d-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f2b4d-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="f2b4d-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2b4d-148">NOTES</span></span>

## <span data-ttu-id="f2b4d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2b4d-149">RELATED LINKS</span></span>

[<span data-ttu-id="f2b4d-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f2b4d-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="f2b4d-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f2b4d-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f2b4d-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f2b4d-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
