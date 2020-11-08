---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044814"
---
# <span data-ttu-id="7c10e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7c10e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="7c10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c10e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c10e-103">RuleGroupOverrideGroup entry에 대 한 managedRuleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="7c10e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c10e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c10e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c10e-105">DESCRIPTION</span></span>
<span data-ttu-id="7c10e-106">**AzApplicationGatewayFirewallPolicyManagedRuleOverride** 는 ruleoverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="7c10e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c10e-107">EXAMPLES</span></span>

### <span data-ttu-id="7c10e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c10e-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="7c10e-109">RuleId로 $ruleId 및 상태가 비활성으로 설정 된 ruleOverride 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="7c10e-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c10e-110">PARAMETERS</span></span>

### <span data-ttu-id="7c10e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c10e-111">-DefaultProfile</span></span>
<span data-ttu-id="7c10e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c10e-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="7c10e-113">-RuleId</span></span>
<span data-ttu-id="7c10e-114">재정의 규칙 항목에 RuleId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="7c10e-115">-상태</span><span class="sxs-lookup"><span data-stu-id="7c10e-115">-State</span></span>
<span data-ttu-id="7c10e-116">재정의 규칙 항목에 RuleId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="7c10e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c10e-117">CommonParameters</span></span>
<span data-ttu-id="7c10e-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c10e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c10e-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c10e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c10e-120">입력</span><span class="sxs-lookup"><span data-stu-id="7c10e-120">INPUTS</span></span>

### <span data-ttu-id="7c10e-121">않아야</span><span class="sxs-lookup"><span data-stu-id="7c10e-121">None</span></span>

## <span data-ttu-id="7c10e-122">출력</span><span class="sxs-lookup"><span data-stu-id="7c10e-122">OUTPUTS</span></span>

### <span data-ttu-id="7c10e-123">PSApplicationGatewayFirewallPolicyManagedRuleOverride에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7c10e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="7c10e-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7c10e-124">NOTES</span></span>

## <span data-ttu-id="7c10e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c10e-125">RELATED LINKS</span></span>
