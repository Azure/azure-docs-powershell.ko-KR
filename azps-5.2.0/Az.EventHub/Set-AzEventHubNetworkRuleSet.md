---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354393"
---
# <span data-ttu-id="178f6-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="178f6-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="178f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178f6-102">SYNOPSIS</span></span>
<span data-ttu-id="178f6-103">현재 Azure 구독에서 주어진 네임스페이스의 NetworkruleSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="178f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="178f6-104">SYNTAX</span></span>

### <span data-ttu-id="178f6-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="178f6-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="178f6-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="178f6-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="178f6-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="178f6-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178f6-108">설명</span><span class="sxs-lookup"><span data-stu-id="178f6-108">DESCRIPTION</span></span>
<span data-ttu-id="178f6-109">현재 Azure 구독에서 주어진 네임스페이스의 NetworkruleSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="178f6-110">예제</span><span class="sxs-lookup"><span data-stu-id="178f6-110">EXAMPLES</span></span>

### <span data-ttu-id="178f6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="178f6-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="178f6-112">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="178f6-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="178f6-113">-IPRule 및 -VirtualNetworkRule 매개 변수를 사용하여 NetworkRuleSet 업데이트</span><span class="sxs-lookup"><span data-stu-id="178f6-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="178f6-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="178f6-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="178f6-115">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="178f6-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="178f6-116">-InputObject를 사용하여 NetworkRuleSet 업데이트</span><span class="sxs-lookup"><span data-stu-id="178f6-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="178f6-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="178f6-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="178f6-118">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="178f6-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="178f6-119">다른 네임스페이스의 -ResourceId를 사용하여 NetworkRuleSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="178f6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="178f6-120">PARAMETERS</span></span>

### <span data-ttu-id="178f6-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="178f6-121">-DefaultAction</span></span>
<span data-ttu-id="178f6-122">NetworkRuleSet에 대한 기본 작업</span><span class="sxs-lookup"><span data-stu-id="178f6-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178f6-123">-DefaultProfile</span></span>
<span data-ttu-id="178f6-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="178f6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="178f6-125">-InputObject</span></span>
<span data-ttu-id="178f6-126">NetworkruleSet 구성 개체</span><span class="sxs-lookup"><span data-stu-id="178f6-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="178f6-127">-IPRule</span></span>
<span data-ttu-id="178f6-128">IPRuleSet 목록</span><span class="sxs-lookup"><span data-stu-id="178f6-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-129">-Name</span><span class="sxs-lookup"><span data-stu-id="178f6-129">-Name</span></span>
<span data-ttu-id="178f6-130">EventHub 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178f6-131">-ResourceGroupName</span></span>
<span data-ttu-id="178f6-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="178f6-133">-ResourceId</span></span>
<span data-ttu-id="178f6-134">네임스페이스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="178f6-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="178f6-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="178f6-136">TrustedServiceAccessEnabled를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="178f6-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="178f6-138">VirtualNetworkRules 목록</span><span class="sxs-lookup"><span data-stu-id="178f6-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178f6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="178f6-139">-Confirm</span></span>
<span data-ttu-id="178f6-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="178f6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178f6-141">-WhatIf</span></span>
<span data-ttu-id="178f6-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="178f6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178f6-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="178f6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178f6-144">CommonParameters</span></span>
<span data-ttu-id="178f6-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178f6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="178f6-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178f6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178f6-147">입력</span><span class="sxs-lookup"><span data-stu-id="178f6-147">INPUTS</span></span>

### <span data-ttu-id="178f6-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="178f6-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="178f6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="178f6-149">System.String</span></span>

## <span data-ttu-id="178f6-150">출력</span><span class="sxs-lookup"><span data-stu-id="178f6-150">OUTPUTS</span></span>

### <span data-ttu-id="178f6-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="178f6-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="178f6-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="178f6-152">NOTES</span></span>

## <span data-ttu-id="178f6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="178f6-153">RELATED LINKS</span></span>