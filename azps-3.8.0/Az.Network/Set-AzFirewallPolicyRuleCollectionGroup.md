---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042509"
---
# <span data-ttu-id="ba8c0-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="ba8c0-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ba8c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8c0-103">수정 된 azure 방화벽 정책 규칙 모음 그룹을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="ba8c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba8c0-104">SYNTAX</span></span>

### <span data-ttu-id="ba8c0-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8c0-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba8c0-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8c0-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba8c0-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8c0-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba8c0-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8c0-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba8c0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ba8c0-109">DESCRIPTION</span></span>
<span data-ttu-id="ba8c0-110">**AzFirewallPolicyRuleCollectionGroup** Cmdlet은 Azure 방화벽 정책의 규칙 컬렉션 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ba8c0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ba8c0-111">EXAMPLES</span></span>

### <span data-ttu-id="ba8c0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba8c0-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="ba8c0-113">이 예제에서는 방화벽 정책의 규칙 모음 그룹을 업데이트 $fp</span><span class="sxs-lookup"><span data-stu-id="ba8c0-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="ba8c0-114">변수</span><span class="sxs-lookup"><span data-stu-id="ba8c0-114">PARAMETERS</span></span>

### <span data-ttu-id="ba8c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8c0-115">-DefaultProfile</span></span>
<span data-ttu-id="ba8c0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba8c0-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="ba8c0-117">-FirewallPolicyName</span></span>
<span data-ttu-id="ba8c0-118">방화벽 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="ba8c0-118">The name of the firewall policy</span></span>

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

### <span data-ttu-id="ba8c0-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ba8c0-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="ba8c0-120">방화벽 정책.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8c0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba8c0-121">-InputObject</span></span>
<span data-ttu-id="ba8c0-122">규칙 목록</span><span class="sxs-lookup"><span data-stu-id="ba8c0-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8c0-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ba8c0-123">-Name</span></span>
<span data-ttu-id="ba8c0-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8c0-125">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="ba8c0-125">-Priority</span></span>
<span data-ttu-id="ba8c0-126">규칙 그룹의 우선 순위</span><span class="sxs-lookup"><span data-stu-id="ba8c0-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba8c0-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-128">The resource group name.</span></span>

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

### <span data-ttu-id="ba8c0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba8c0-129">-ResourceId</span></span>
<span data-ttu-id="ba8c0-130">규칙 컬렉션 groupy의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8c0-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="ba8c0-131">-RuleCollection</span></span>
<span data-ttu-id="ba8c0-132">규칙 컬렉션 목록</span><span class="sxs-lookup"><span data-stu-id="ba8c0-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8c0-133">-확인</span><span class="sxs-lookup"><span data-stu-id="ba8c0-133">-Confirm</span></span>
<span data-ttu-id="ba8c0-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8c0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8c0-135">-WhatIf</span></span>
<span data-ttu-id="ba8c0-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8c0-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8c0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8c0-138">CommonParameters</span></span>
<span data-ttu-id="ba8c0-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8c0-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8c0-141">입력</span><span class="sxs-lookup"><span data-stu-id="ba8c0-141">INPUTS</span></span>

### <span data-ttu-id="ba8c0-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba8c0-142">System.String</span></span>

### <span data-ttu-id="ba8c0-143">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="ba8c0-144">출력</span><span class="sxs-lookup"><span data-stu-id="ba8c0-144">OUTPUTS</span></span>

### <span data-ttu-id="ba8c0-145">PSAzureFirewallPolicyRuleCollectionGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ba8c0-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="ba8c0-146">상속자</span><span class="sxs-lookup"><span data-stu-id="ba8c0-146">NOTES</span></span>

## <span data-ttu-id="ba8c0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba8c0-147">RELATED LINKS</span></span>
