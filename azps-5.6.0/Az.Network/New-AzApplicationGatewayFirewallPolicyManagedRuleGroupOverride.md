---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 6b105ab242f9ffb64d1d523cad5930c48714c724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001163"
---
# <span data-ttu-id="458bc-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="458bc-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="458bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458bc-102">SYNOPSIS</span></span>
<span data-ttu-id="458bc-103">방화벽 정책에 대한 ManagedRuleSets에서 RuleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="458bc-104">구문</span><span class="sxs-lookup"><span data-stu-id="458bc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="458bc-105">설명</span><span class="sxs-lookup"><span data-stu-id="458bc-105">DESCRIPTION</span></span>
<span data-ttu-id="458bc-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride는** 방화벽 정책에 대한 managedRuleSet에서 ruleGroupOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="458bc-107">예제</span><span class="sxs-lookup"><span data-stu-id="458bc-107">EXAMPLES</span></span>

### <span data-ttu-id="458bc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="458bc-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="458bc-109">그룹 이름으로 RuleGroupOverride 항목을 $ruleName 및 규칙은 $rule 1, $rule 2로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="458bc-110">동일한 할당을 $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="458bc-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="458bc-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="458bc-111">PARAMETERS</span></span>

### <span data-ttu-id="458bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458bc-112">-DefaultProfile</span></span>
<span data-ttu-id="458bc-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="458bc-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="458bc-114">-Rule</span></span>
<span data-ttu-id="458bc-115">규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-115">List of Rules.</span></span>

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

### <span data-ttu-id="458bc-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="458bc-116">-RuleGroupName</span></span>
<span data-ttu-id="458bc-117">재지정 RuleGroup 항목에서 ruleGroupName을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="458bc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458bc-118">CommonParameters</span></span>
<span data-ttu-id="458bc-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="458bc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458bc-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="458bc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458bc-121">입력</span><span class="sxs-lookup"><span data-stu-id="458bc-121">INPUTS</span></span>

### <span data-ttu-id="458bc-122">없음</span><span class="sxs-lookup"><span data-stu-id="458bc-122">None</span></span>

## <span data-ttu-id="458bc-123">출력</span><span class="sxs-lookup"><span data-stu-id="458bc-123">OUTPUTS</span></span>

### <span data-ttu-id="458bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="458bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="458bc-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="458bc-125">NOTES</span></span>

## <span data-ttu-id="458bc-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="458bc-126">RELATED LINKS</span></span>
