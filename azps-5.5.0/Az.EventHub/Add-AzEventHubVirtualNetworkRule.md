---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209584"
---
# <span data-ttu-id="e87c4-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e87c4-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="e87c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e87c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e87c4-103">주어진 네임스페이스에 대한 NetworkRuleSet에 단일 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="e87c4-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="e87c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="e87c4-104">SYNTAX</span></span>

### <span data-ttu-id="e87c4-105">VirtualNetworkRulePropertiesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e87c4-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e87c4-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e87c4-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87c4-107">설명</span><span class="sxs-lookup"><span data-stu-id="e87c4-107">DESCRIPTION</span></span>
<span data-ttu-id="e87c4-108">주어진 네임스페이스에 대한 NetworkRuleSet에 단일 VirtualNetworkRule 추가</span><span class="sxs-lookup"><span data-stu-id="e87c4-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="e87c4-109">예제</span><span class="sxs-lookup"><span data-stu-id="e87c4-109">EXAMPLES</span></span>

### <span data-ttu-id="e87c4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e87c4-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="e87c4-111">이름 : defaultAction : 허용 ID : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="e87c4-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="e87c4-112">주어진 네임스페이스에 대해 주어진 서브넷 및 IgnoreMissingVnetServiceEndpoint(VirtualNetworkRule)를 NetworkRuleSet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c4-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="e87c4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e87c4-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="e87c4-114">이름 : defaultAction : 허용 ID : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="e87c4-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="e87c4-115">주어진 네임스페이스에 $virtualruleset 1을 NetworkRuleSet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c4-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="e87c4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e87c4-116">PARAMETERS</span></span>

### <span data-ttu-id="e87c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87c4-117">-DefaultProfile</span></span>
<span data-ttu-id="e87c4-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e87c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e87c4-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e87c4-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e87c4-120">ARM ID of Subnet</span><span class="sxs-lookup"><span data-stu-id="e87c4-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87c4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e87c4-121">-Name</span></span>
<span data-ttu-id="e87c4-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e87c4-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e87c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e87c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="e87c4-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e87c4-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e87c4-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e87c4-125">-SubnetId</span></span>
<span data-ttu-id="e87c4-126">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e87c4-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e87c4-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e87c4-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e87c4-128">VirtualNetworkRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="e87c4-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e87c4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e87c4-129">-Confirm</span></span>
<span data-ttu-id="e87c4-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e87c4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87c4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87c4-131">-WhatIf</span></span>
<span data-ttu-id="e87c4-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e87c4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e87c4-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e87c4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87c4-134">CommonParameters</span></span>
<span data-ttu-id="e87c4-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e87c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e87c4-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e87c4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87c4-137">입력</span><span class="sxs-lookup"><span data-stu-id="e87c4-137">INPUTS</span></span>

### <span data-ttu-id="e87c4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e87c4-138">System.String</span></span>

### <span data-ttu-id="e87c4-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e87c4-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e87c4-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e87c4-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="e87c4-141">출력</span><span class="sxs-lookup"><span data-stu-id="e87c4-141">OUTPUTS</span></span>

### <span data-ttu-id="e87c4-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="e87c4-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="e87c4-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e87c4-143">NOTES</span></span>

## <span data-ttu-id="e87c4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e87c4-144">RELATED LINKS</span></span>
