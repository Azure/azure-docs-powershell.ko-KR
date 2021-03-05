---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992642"
---
# <span data-ttu-id="2965d-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2965d-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="2965d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2965d-102">SYNOPSIS</span></span>
<span data-ttu-id="2965d-103">RuleGroupOverrideGroup 항목에 대해 managedRuleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="2965d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2965d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2965d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2965d-105">DESCRIPTION</span></span>
<span data-ttu-id="2965d-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride는** ruleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="2965d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2965d-107">EXAMPLES</span></span>

### <span data-ttu-id="2965d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2965d-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="2965d-109">RuleId를 사용 안 으로 설정하고 $ruleId 상태로 ruleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="2965d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2965d-110">PARAMETERS</span></span>

### <span data-ttu-id="2965d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2965d-111">-DefaultProfile</span></span>
<span data-ttu-id="2965d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2965d-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="2965d-113">-RuleId</span></span>
<span data-ttu-id="2965d-114">규칙 항목을 재지정할 때 RuleId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="2965d-115">-State</span><span class="sxs-lookup"><span data-stu-id="2965d-115">-State</span></span>
<span data-ttu-id="2965d-116">규칙 항목을 재지정할 때 RuleId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="2965d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2965d-117">CommonParameters</span></span>
<span data-ttu-id="2965d-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2965d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2965d-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2965d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2965d-120">입력</span><span class="sxs-lookup"><span data-stu-id="2965d-120">INPUTS</span></span>

### <span data-ttu-id="2965d-121">없음</span><span class="sxs-lookup"><span data-stu-id="2965d-121">None</span></span>

## <span data-ttu-id="2965d-122">출력</span><span class="sxs-lookup"><span data-stu-id="2965d-122">OUTPUTS</span></span>

### <span data-ttu-id="2965d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2965d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="2965d-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2965d-124">NOTES</span></span>

## <span data-ttu-id="2965d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2965d-125">RELATED LINKS</span></span>
