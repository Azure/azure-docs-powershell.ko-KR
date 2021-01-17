---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379457"
---
# <span data-ttu-id="b7fed-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7fed-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="b7fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7fed-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fed-103">firewallPolicy에 대한 ManagedRuleSet을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7fed-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="b7fed-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7fed-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7fed-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7fed-105">DESCRIPTION</span></span>
<span data-ttu-id="b7fed-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleSet은** 방화벽 정책에 대한 관리 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7fed-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="b7fed-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7fed-107">EXAMPLES</span></span>

### <span data-ttu-id="b7fed-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7fed-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="b7fed-109">ruleSetType을 $ruleSetType, ruleSetVersion을 $ruleSetVersion로, ruleGroupOverrides를 $ruleGroupOverride 1, $ruleGroupOverride 2 새 ManagedRuleSet이 새 ManagedRuleSet에 할당된 목록으로 $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7fed-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="b7fed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7fed-110">PARAMETERS</span></span>

### <span data-ttu-id="b7fed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fed-111">-DefaultProfile</span></span>
<span data-ttu-id="b7fed-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7fed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fed-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b7fed-113">-RuleGroupOverride</span></span>
<span data-ttu-id="b7fed-114">규칙 그룹이 오버라이드됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7fed-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fed-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="b7fed-115">-RuleSetType</span></span>
<span data-ttu-id="b7fed-116">managedRuleSet에서 RuleSetType 지정</span><span class="sxs-lookup"><span data-stu-id="b7fed-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="b7fed-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="b7fed-117">-RuleSetVersion</span></span>
<span data-ttu-id="b7fed-118">managedRuleSet에서 RuleSetVersion 지정</span><span class="sxs-lookup"><span data-stu-id="b7fed-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="b7fed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fed-119">CommonParameters</span></span>
<span data-ttu-id="b7fed-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7fed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fed-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7fed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fed-122">입력</span><span class="sxs-lookup"><span data-stu-id="b7fed-122">INPUTS</span></span>

### <span data-ttu-id="b7fed-123">없음</span><span class="sxs-lookup"><span data-stu-id="b7fed-123">None</span></span>

## <span data-ttu-id="b7fed-124">출력</span><span class="sxs-lookup"><span data-stu-id="b7fed-124">OUTPUTS</span></span>

### <span data-ttu-id="b7fed-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7fed-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="b7fed-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7fed-126">NOTES</span></span>

## <span data-ttu-id="b7fed-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7fed-127">RELATED LINKS</span></span>
