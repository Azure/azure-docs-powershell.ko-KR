---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041812"
---
# <span data-ttu-id="b0502-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="b0502-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="b0502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0502-102">SYNOPSIS</span></span>
<span data-ttu-id="b0502-103">새 Azure 방화벽 정책 규칙 모음 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="b0502-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="b0502-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0502-104">SYNTAX</span></span>

### <span data-ttu-id="b0502-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0502-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0502-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0502-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0502-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0502-107">DESCRIPTION</span></span>
<span data-ttu-id="b0502-108">**AzFirewallPolicyRuleCollectionGroup** Cmdlet은 Azure 방화벽 정책에서 규칙 모음 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="b0502-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b0502-109">EXAMPLES</span></span>

### <span data-ttu-id="b0502-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0502-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="b0502-111">이 예제에서는 방화벽 정책에서 규칙 모음 그룹을 만듭니다 $fp</span><span class="sxs-lookup"><span data-stu-id="b0502-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="b0502-112">변수</span><span class="sxs-lookup"><span data-stu-id="b0502-112">PARAMETERS</span></span>

### <span data-ttu-id="b0502-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0502-113">-DefaultProfile</span></span>
<span data-ttu-id="b0502-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0502-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="b0502-115">-FirewallPolicyName</span></span>
<span data-ttu-id="b0502-116">방화벽 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="b0502-116">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b0502-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="b0502-118">방화벽 정책.</span><span class="sxs-lookup"><span data-stu-id="b0502-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b0502-119">-Name</span></span>
<span data-ttu-id="b0502-120">규칙 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-120">The name of the Rule Group</span></span>

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

### <span data-ttu-id="b0502-121">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="b0502-121">-Priority</span></span>
<span data-ttu-id="b0502-122">규칙 그룹의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="b0502-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0502-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0502-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="b0502-125">-RuleCollection</span></span>
<span data-ttu-id="b0502-126">규칙 목록</span><span class="sxs-lookup"><span data-stu-id="b0502-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-127">-확인</span><span class="sxs-lookup"><span data-stu-id="b0502-127">-Confirm</span></span>
<span data-ttu-id="b0502-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0502-129">-WhatIf</span></span>
<span data-ttu-id="b0502-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0502-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0502-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0502-132">CommonParameters</span></span>
<span data-ttu-id="b0502-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0502-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0502-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0502-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0502-135">입력</span><span class="sxs-lookup"><span data-stu-id="b0502-135">INPUTS</span></span>

### <span data-ttu-id="b0502-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0502-136">System.String</span></span>

### <span data-ttu-id="b0502-137">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b0502-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="b0502-138">출력</span><span class="sxs-lookup"><span data-stu-id="b0502-138">OUTPUTS</span></span>

### <span data-ttu-id="b0502-139">PSAzureFirewallPolicyRuleCollectionGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b0502-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="b0502-140">상속자</span><span class="sxs-lookup"><span data-stu-id="b0502-140">NOTES</span></span>

## <span data-ttu-id="b0502-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0502-141">RELATED LINKS</span></span>
