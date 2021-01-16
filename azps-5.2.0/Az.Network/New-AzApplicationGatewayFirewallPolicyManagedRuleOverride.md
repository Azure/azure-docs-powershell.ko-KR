---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340233"
---
# <span data-ttu-id="26500-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="26500-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="26500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26500-102">SYNOPSIS</span></span>
<span data-ttu-id="26500-103">RuleGroupOverrideGroup 항목에 대한 managedRuleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26500-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="26500-104">구문</span><span class="sxs-lookup"><span data-stu-id="26500-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26500-105">설명</span><span class="sxs-lookup"><span data-stu-id="26500-105">DESCRIPTION</span></span>
<span data-ttu-id="26500-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride는** ruleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26500-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="26500-107">예제</span><span class="sxs-lookup"><span data-stu-id="26500-107">EXAMPLES</span></span>

### <span data-ttu-id="26500-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="26500-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="26500-109">RuleId를 사용 안 으로 설정하고 상태를 사용 안 $ruleId ruleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26500-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="26500-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26500-110">PARAMETERS</span></span>

### <span data-ttu-id="26500-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26500-111">-DefaultProfile</span></span>
<span data-ttu-id="26500-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26500-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26500-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="26500-113">-RuleId</span></span>
<span data-ttu-id="26500-114">규칙 항목의 RuleId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26500-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="26500-115">-State</span><span class="sxs-lookup"><span data-stu-id="26500-115">-State</span></span>
<span data-ttu-id="26500-116">규칙 항목의 RuleId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26500-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26500-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26500-117">CommonParameters</span></span>
<span data-ttu-id="26500-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26500-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26500-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26500-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26500-120">입력</span><span class="sxs-lookup"><span data-stu-id="26500-120">INPUTS</span></span>

### <span data-ttu-id="26500-121">없음</span><span class="sxs-lookup"><span data-stu-id="26500-121">None</span></span>

## <span data-ttu-id="26500-122">출력</span><span class="sxs-lookup"><span data-stu-id="26500-122">OUTPUTS</span></span>

### <span data-ttu-id="26500-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="26500-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="26500-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26500-124">NOTES</span></span>

## <span data-ttu-id="26500-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26500-125">RELATED LINKS</span></span>
