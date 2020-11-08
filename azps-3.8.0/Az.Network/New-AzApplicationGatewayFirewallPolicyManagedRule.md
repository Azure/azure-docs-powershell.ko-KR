---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044816"
---
# <span data-ttu-id="22b69-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="22b69-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="22b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22b69-102">SYNOPSIS</span></span>
<span data-ttu-id="22b69-103">방화벽 정책에 대 한 ManagedRules를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="22b69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22b69-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22b69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22b69-105">DESCRIPTION</span></span>
<span data-ttu-id="22b69-106">**새로운 AzApplicationGatewayFirewallPolicyManagedRule** 는 방화벽 정책에 대 한 관리 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="22b69-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22b69-107">EXAMPLES</span></span>

### <span data-ttu-id="22b69-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="22b69-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="22b69-109">이 명령은 관리 되는 규칙을 $managedRuleSet 및 $exclusion 1 ($exclusion 2)의 항목을 포함 하는 제외 목록에 대 한 ManagedRuleSet 목록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="22b69-110">변수</span><span class="sxs-lookup"><span data-stu-id="22b69-110">PARAMETERS</span></span>

### <span data-ttu-id="22b69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b69-111">-DefaultProfile</span></span>
<span data-ttu-id="22b69-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b69-113">-제외</span><span class="sxs-lookup"><span data-stu-id="22b69-113">-Exclusion</span></span>
<span data-ttu-id="22b69-114">제외 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="22b69-115">-ManagedRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="22b69-115">-ManagedRuleSet</span></span>
<span data-ttu-id="22b69-116">관리 되는 규칙 집합 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="22b69-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b69-117">CommonParameters</span></span>
<span data-ttu-id="22b69-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22b69-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b69-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="22b69-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b69-120">입력</span><span class="sxs-lookup"><span data-stu-id="22b69-120">INPUTS</span></span>

### <span data-ttu-id="22b69-121">않아야</span><span class="sxs-lookup"><span data-stu-id="22b69-121">None</span></span>

## <span data-ttu-id="22b69-122">출력</span><span class="sxs-lookup"><span data-stu-id="22b69-122">OUTPUTS</span></span>

### <span data-ttu-id="22b69-123">PSApplicationGatewayFirewallPolicyManagedRules에 대 한.</span><span class="sxs-lookup"><span data-stu-id="22b69-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="22b69-124">상속자</span><span class="sxs-lookup"><span data-stu-id="22b69-124">NOTES</span></span>

## <span data-ttu-id="22b69-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22b69-125">RELATED LINKS</span></span>
