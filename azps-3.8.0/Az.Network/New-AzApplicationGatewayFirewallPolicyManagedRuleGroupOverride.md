---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044815"
---
# <span data-ttu-id="6580c-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6580c-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="6580c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6580c-102">SYNOPSIS</span></span>
<span data-ttu-id="6580c-103">방화벽 정책에 대 한 ManagedRuleSets 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="6580c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6580c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6580c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6580c-105">DESCRIPTION</span></span>
<span data-ttu-id="6580c-106">**AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** 는 방화벽 정책에 대 한 managedruleset 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="6580c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6580c-107">EXAMPLES</span></span>

### <span data-ttu-id="6580c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6580c-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="6580c-109">$Rule 1 $rule 2) 인 $ruleName 및 규칙으로 그룹 이름이 있는 RuleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="6580c-110">$overrideEntry에 동일 하 게 할당</span><span class="sxs-lookup"><span data-stu-id="6580c-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="6580c-111">변수</span><span class="sxs-lookup"><span data-stu-id="6580c-111">PARAMETERS</span></span>

### <span data-ttu-id="6580c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6580c-112">-DefaultProfile</span></span>
<span data-ttu-id="6580c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6580c-114">-규칙</span><span class="sxs-lookup"><span data-stu-id="6580c-114">-Rule</span></span>
<span data-ttu-id="6580c-115">규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6580c-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="6580c-116">-RuleGroupName</span></span>
<span data-ttu-id="6580c-117">오버라이드 Rulegroupname 항목에서 ruleGroupName을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="6580c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6580c-118">CommonParameters</span></span>
<span data-ttu-id="6580c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6580c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6580c-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6580c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6580c-121">입력</span><span class="sxs-lookup"><span data-stu-id="6580c-121">INPUTS</span></span>

### <span data-ttu-id="6580c-122">않아야</span><span class="sxs-lookup"><span data-stu-id="6580c-122">None</span></span>

## <span data-ttu-id="6580c-123">출력</span><span class="sxs-lookup"><span data-stu-id="6580c-123">OUTPUTS</span></span>

### <span data-ttu-id="6580c-124">PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6580c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="6580c-125">상속자</span><span class="sxs-lookup"><span data-stu-id="6580c-125">NOTES</span></span>

## <span data-ttu-id="6580c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6580c-126">RELATED LINKS</span></span>
