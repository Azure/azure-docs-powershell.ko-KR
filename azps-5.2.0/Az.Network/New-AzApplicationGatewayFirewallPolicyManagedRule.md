---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340238"
---
# <span data-ttu-id="a6fc2-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a6fc2-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="a6fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fc2-103">방화벽 정책에 대한 ManagedRules를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="a6fc2-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6fc2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6fc2-105">설명</span><span class="sxs-lookup"><span data-stu-id="a6fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="a6fc2-106">**New-AzApplicationGatewayFirewallPolicyManagedRule은** 방화벽 정책에 대한 관리 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="a6fc2-107">예제</span><span class="sxs-lookup"><span data-stu-id="a6fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="a6fc2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6fc2-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="a6fc2-109">이 명령은 $managedRuleSet ManagedRuleSet 목록과 $exclusion 1, $exclusion 2와 같은 항목이 있는 제외 목록을 $exclusion.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="a6fc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="a6fc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6fc2-111">-DefaultProfile</span></span>
<span data-ttu-id="a6fc2-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6fc2-113">-제외</span><span class="sxs-lookup"><span data-stu-id="a6fc2-113">-Exclusion</span></span>
<span data-ttu-id="a6fc2-114">제외 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6fc2-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a6fc2-115">-ManagedRuleSet</span></span>
<span data-ttu-id="a6fc2-116">관리되는 ruleSets 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6fc2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fc2-117">CommonParameters</span></span>
<span data-ttu-id="a6fc2-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fc2-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fc2-120">입력</span><span class="sxs-lookup"><span data-stu-id="a6fc2-120">INPUTS</span></span>

### <span data-ttu-id="a6fc2-121">없음</span><span class="sxs-lookup"><span data-stu-id="a6fc2-121">None</span></span>

## <span data-ttu-id="a6fc2-122">출력</span><span class="sxs-lookup"><span data-stu-id="a6fc2-122">OUTPUTS</span></span>

### <span data-ttu-id="a6fc2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="a6fc2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="a6fc2-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6fc2-124">NOTES</span></span>

## <span data-ttu-id="a6fc2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6fc2-125">RELATED LINKS</span></span>
