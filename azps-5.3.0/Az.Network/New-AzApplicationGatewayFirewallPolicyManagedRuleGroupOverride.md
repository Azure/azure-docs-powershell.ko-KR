---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491088"
---
# <span data-ttu-id="2cba2-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2cba2-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="2cba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cba2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cba2-103">방화벽 정책에 대한 ManagedRuleSets에서 RuleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="2cba2-104">구문</span><span class="sxs-lookup"><span data-stu-id="2cba2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cba2-105">설명</span><span class="sxs-lookup"><span data-stu-id="2cba2-105">DESCRIPTION</span></span>
<span data-ttu-id="2cba2-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride는** 방화벽 정책에 대한 managedRuleSet에 ruleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="2cba2-107">예제</span><span class="sxs-lookup"><span data-stu-id="2cba2-107">EXAMPLES</span></span>

### <span data-ttu-id="2cba2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2cba2-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="2cba2-109">$rule 1, $rule 2로 그룹 이름으로 그룹 $ruleName RuleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="2cba2-110">동일한 할당을 $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="2cba2-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="2cba2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cba2-111">PARAMETERS</span></span>

### <span data-ttu-id="2cba2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cba2-112">-DefaultProfile</span></span>
<span data-ttu-id="2cba2-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cba2-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="2cba2-114">-Rule</span></span>
<span data-ttu-id="2cba2-115">규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-115">List of Rules.</span></span>

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

### <span data-ttu-id="2cba2-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="2cba2-116">-RuleGroupName</span></span>
<span data-ttu-id="2cba2-117">RuleGroup 항목의 ruleGroupName을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="2cba2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cba2-118">CommonParameters</span></span>
<span data-ttu-id="2cba2-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2cba2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cba2-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2cba2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cba2-121">입력</span><span class="sxs-lookup"><span data-stu-id="2cba2-121">INPUTS</span></span>

### <span data-ttu-id="2cba2-122">없음</span><span class="sxs-lookup"><span data-stu-id="2cba2-122">None</span></span>

## <span data-ttu-id="2cba2-123">출력</span><span class="sxs-lookup"><span data-stu-id="2cba2-123">OUTPUTS</span></span>

### <span data-ttu-id="2cba2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2cba2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="2cba2-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2cba2-125">NOTES</span></span>

## <span data-ttu-id="2cba2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cba2-126">RELATED LINKS</span></span>
