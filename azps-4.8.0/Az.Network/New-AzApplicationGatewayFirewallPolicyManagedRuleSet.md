---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203988"
---
# <span data-ttu-id="5c05f-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c05f-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="5c05f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c05f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c05f-103">FirewallPolicy에 대 한 ManagedRuleSet 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c05f-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="5c05f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c05f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c05f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c05f-105">DESCRIPTION</span></span>
<span data-ttu-id="5c05f-106">**새로운 AzApplicationGatewayFirewallPolicyManagedRuleSet** 는 방화벽 정책에 대 한 관리 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c05f-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="5c05f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5c05f-107">EXAMPLES</span></span>

### <span data-ttu-id="5c05f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c05f-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="5c05f-109">RuleSetType을 $ruleSetType로 사용 하 고 $ruleSetVersion와 RuleGroupOverrides로 Rulesettype을 $ruleGroupOverride 1로 표시 하는 목록으로, $ruleGroupOverride 2 인 새 ManagedRuleSet 집합이 지정 되어 $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c05f-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="5c05f-110">변수</span><span class="sxs-lookup"><span data-stu-id="5c05f-110">PARAMETERS</span></span>

### <span data-ttu-id="5c05f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c05f-111">-DefaultProfile</span></span>
<span data-ttu-id="5c05f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c05f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c05f-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="5c05f-113">-RuleGroupOverride</span></span>
<span data-ttu-id="5c05f-114">규칙 그룹 재정의</span><span class="sxs-lookup"><span data-stu-id="5c05f-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="5c05f-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="5c05f-115">-RuleSetType</span></span>
<span data-ttu-id="5c05f-116">Managedsettype을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c05f-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="5c05f-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="5c05f-117">-RuleSetVersion</span></span>
<span data-ttu-id="5c05f-118">Managedsetversion에 대 한 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c05f-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="5c05f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c05f-119">CommonParameters</span></span>
<span data-ttu-id="5c05f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c05f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c05f-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c05f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c05f-122">입력</span><span class="sxs-lookup"><span data-stu-id="5c05f-122">INPUTS</span></span>

### <span data-ttu-id="5c05f-123">않아야</span><span class="sxs-lookup"><span data-stu-id="5c05f-123">None</span></span>

## <span data-ttu-id="5c05f-124">출력</span><span class="sxs-lookup"><span data-stu-id="5c05f-124">OUTPUTS</span></span>

### <span data-ttu-id="5c05f-125">PSApplicationGatewayFirewallPolicyManagedRuleSet에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5c05f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="5c05f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5c05f-126">NOTES</span></span>

## <span data-ttu-id="5c05f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c05f-127">RELATED LINKS</span></span>
