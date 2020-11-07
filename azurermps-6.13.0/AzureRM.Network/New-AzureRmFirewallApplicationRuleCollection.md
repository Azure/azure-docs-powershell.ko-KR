---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711333"
---
# <span data-ttu-id="bb7d5-101">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bb7d5-101">New-AzureRmFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="bb7d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7d5-103">방화벽 응용 프로그램 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-103">Creates a collection of Firewall application rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb7d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb7d5-104">SYNTAX</span></span>

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb7d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="bb7d5-106">**AzureRmFirewallApplicationRuleCollection** Cmdlet은 방화벽 응용 프로그램 규칙의 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-106">The **New-AzureRmFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="bb7d5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb7d5-107">EXAMPLES</span></span>

### <span data-ttu-id="bb7d5-108">1: 규칙 하나를 사용 하 여 컬렉션 만들기</span><span class="sxs-lookup"><span data-stu-id="bb7d5-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="bb7d5-109">이 예제에서는 하나의 규칙이 있는 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="bb7d5-110">$Rule 1에서 식별 된 조건과 일치 하는 모든 트래픽이 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="bb7d5-111">첫 번째 규칙은 10.0.0.0에서 포트 443의 모든 HTTPS 트래픽에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="bb7d5-112">우선 순위가 높은 다른 응용 프로그램 규칙 모음 (더 적은 수)이 있는 경우 $rule 1에서 식별 된 트래픽에만 일치 하는 경우에는 우선 순위가 높은 규칙 모음의 작업이 대신 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="bb7d5-113">2: 규칙 컬렉션에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="bb7d5-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="bb7d5-114">이 예제에서는 규칙 하나가 있는 새 응용 프로그램 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에 메서드 AddRule을 사용 하 여 규칙 컬렉션에 두 번째 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="bb7d5-115">지정 된 규칙 컬렉션의 각 규칙 이름은 고유한 이름을 가져야 하 고 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="bb7d5-116">3: 규칙 컬렉션에서 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="bb7d5-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="bb7d5-117">이 예제에서는 규칙 하나가 있는 새 응용 프로그램 규칙 컬렉션을 만든 다음 이름으로 규칙을 가져오고, 규칙 컬렉션 개체에서 GetRuleByName 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="bb7d5-118">메서드 GetRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="bb7d5-119">4: 규칙 컬렉션에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="bb7d5-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="bb7d5-120">이 예제에서는 두 개의 규칙이 있는 새 응용 프로그램 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체의 메서드 RemoveRuleByName를 호출 하 여 규칙 컬렉션에서 첫 번째 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="bb7d5-121">메서드 RemoveRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="bb7d5-122">변수</span><span class="sxs-lookup"><span data-stu-id="bb7d5-122">PARAMETERS</span></span>

### <span data-ttu-id="bb7d5-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="bb7d5-123">-ActionType</span></span>
<span data-ttu-id="bb7d5-124">규칙 컬렉션의 동작</span><span class="sxs-lookup"><span data-stu-id="bb7d5-124">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7d5-125">-DefaultProfile</span></span>
<span data-ttu-id="bb7d5-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb7d5-127">-이름</span><span class="sxs-lookup"><span data-stu-id="bb7d5-127">-Name</span></span>
<span data-ttu-id="bb7d5-128">이 응용 프로그램 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="bb7d5-129">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="bb7d5-130">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="bb7d5-130">-Priority</span></span>
<span data-ttu-id="bb7d5-131">이 규칙의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="bb7d5-132">Priority는 100과 65000 사이의 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="bb7d5-133">숫자가 작을수록 우선 순위가 커집니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-133">The smaller the number, the bigger the priority.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7d5-134">-규칙</span><span class="sxs-lookup"><span data-stu-id="bb7d5-134">-Rule</span></span>
<span data-ttu-id="bb7d5-135">이 컬렉션 아래에서 그룹화 할 규칙 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7d5-136">-확인</span><span class="sxs-lookup"><span data-stu-id="bb7d5-136">-Confirm</span></span>
<span data-ttu-id="bb7d5-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb7d5-138">-WhatIf</span></span>
<span data-ttu-id="bb7d5-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb7d5-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb7d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7d5-141">CommonParameters</span></span>
<span data-ttu-id="bb7d5-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7d5-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb7d5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7d5-144">입력</span><span class="sxs-lookup"><span data-stu-id="bb7d5-144">INPUTS</span></span>

### <span data-ttu-id="bb7d5-145">않아야</span><span class="sxs-lookup"><span data-stu-id="bb7d5-145">None</span></span>
<span data-ttu-id="bb7d5-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb7d5-147">출력</span><span class="sxs-lookup"><span data-stu-id="bb7d5-147">OUTPUTS</span></span>

### <span data-ttu-id="bb7d5-148">PSFirewallApplicationRuleCollection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bb7d5-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="bb7d5-149">상속자</span><span class="sxs-lookup"><span data-stu-id="bb7d5-149">NOTES</span></span>

## <span data-ttu-id="bb7d5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb7d5-150">RELATED LINKS</span></span>

[<span data-ttu-id="bb7d5-151">새로운 AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="bb7d5-151">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="bb7d5-152">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="bb7d5-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="bb7d5-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="bb7d5-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
