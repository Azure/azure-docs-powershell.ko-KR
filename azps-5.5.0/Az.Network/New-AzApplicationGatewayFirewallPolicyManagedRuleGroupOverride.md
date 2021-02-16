---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179748"
---
# <span data-ttu-id="75429-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="75429-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="75429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75429-102">SYNOPSIS</span></span>
<span data-ttu-id="75429-103">방화벽 정책에 대한 ManagedRuleSets에서 RuleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75429-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="75429-104">구문</span><span class="sxs-lookup"><span data-stu-id="75429-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75429-105">설명</span><span class="sxs-lookup"><span data-stu-id="75429-105">DESCRIPTION</span></span>
<span data-ttu-id="75429-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride는** 방화벽 정책에 대한 managedRuleSet에 ruleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75429-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="75429-107">예제</span><span class="sxs-lookup"><span data-stu-id="75429-107">EXAMPLES</span></span>

### <span data-ttu-id="75429-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="75429-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="75429-109">$rule 1, $rule 2로 그룹 이름으로 그룹 $ruleName RuleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75429-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="75429-110">동일한 할당을 $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="75429-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="75429-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75429-111">PARAMETERS</span></span>

### <span data-ttu-id="75429-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75429-112">-DefaultProfile</span></span>
<span data-ttu-id="75429-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75429-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75429-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="75429-114">-Rule</span></span>
<span data-ttu-id="75429-115">규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="75429-115">List of Rules.</span></span>

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

### <span data-ttu-id="75429-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="75429-116">-RuleGroupName</span></span>
<span data-ttu-id="75429-117">RuleGroup 항목의 ruleGroupName을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75429-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="75429-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75429-118">CommonParameters</span></span>
<span data-ttu-id="75429-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75429-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75429-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75429-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75429-121">입력</span><span class="sxs-lookup"><span data-stu-id="75429-121">INPUTS</span></span>

### <span data-ttu-id="75429-122">없음</span><span class="sxs-lookup"><span data-stu-id="75429-122">None</span></span>

## <span data-ttu-id="75429-123">출력</span><span class="sxs-lookup"><span data-stu-id="75429-123">OUTPUTS</span></span>

### <span data-ttu-id="75429-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="75429-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="75429-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75429-125">NOTES</span></span>

## <span data-ttu-id="75429-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75429-126">RELATED LINKS</span></span>
