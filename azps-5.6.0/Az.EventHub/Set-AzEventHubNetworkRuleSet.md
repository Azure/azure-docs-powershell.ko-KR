---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: b8027083225b774d1795d8c96132a0e031f8a51e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007899"
---
# <span data-ttu-id="ecb49-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecb49-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="ecb49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb49-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb49-103">현재 Azure 구독에서 주어진 네임스페이스의 NetworkruleSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ecb49-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecb49-104">SYNTAX</span></span>

### <span data-ttu-id="ecb49-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ecb49-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb49-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecb49-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb49-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecb49-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecb49-108">설명</span><span class="sxs-lookup"><span data-stu-id="ecb49-108">DESCRIPTION</span></span>
<span data-ttu-id="ecb49-109">현재 Azure 구독에서 주어진 네임스페이스의 NetworkruleSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ecb49-110">예제</span><span class="sxs-lookup"><span data-stu-id="ecb49-110">EXAMPLES</span></span>

### <span data-ttu-id="ecb49-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecb49-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="ecb49-112">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespaces-1122/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, 허용, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="ecb49-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ecb49-113">-IPRule 및 -VirtualNetworkRule 매개 변수를 사용하여 NetworkRuleSet 업데이트</span><span class="sxs-lookup"><span data-stu-id="ecb49-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="ecb49-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ecb49-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="ecb49-115">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespaces-1122/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, 허용, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="ecb49-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ecb49-116">-InputObject를 사용하여 NetworkRuleSet 업데이트</span><span class="sxs-lookup"><span data-stu-id="ecb49-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="ecb49-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="ecb49-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="ecb49-118">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespaces-1122/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, 허용, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="ecb49-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="ecb49-119">다른 네임스페이스의 -ResourceId를 사용하여 NetworkRuleSet을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="ecb49-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecb49-120">PARAMETERS</span></span>

### <span data-ttu-id="ecb49-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ecb49-121">-DefaultAction</span></span>
<span data-ttu-id="ecb49-122">NetworkRuleSet에 대한 기본 작업</span><span class="sxs-lookup"><span data-stu-id="ecb49-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="ecb49-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb49-123">-DefaultProfile</span></span>
<span data-ttu-id="ecb49-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecb49-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb49-125">-InputObject</span></span>
<span data-ttu-id="ecb49-126">NetworkruleSet 구성 개체</span><span class="sxs-lookup"><span data-stu-id="ecb49-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="ecb49-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ecb49-127">-IPRule</span></span>
<span data-ttu-id="ecb49-128">IPRuleSet 목록</span><span class="sxs-lookup"><span data-stu-id="ecb49-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="ecb49-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ecb49-129">-Name</span></span>
<span data-ttu-id="ecb49-130">EventHub 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="ecb49-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb49-131">-ResourceGroupName</span></span>
<span data-ttu-id="ecb49-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="ecb49-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecb49-133">-ResourceId</span></span>
<span data-ttu-id="ecb49-134">네임스페이스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ecb49-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="ecb49-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="ecb49-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="ecb49-136">TrustedServiceAccessEnabled를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

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

### <span data-ttu-id="ecb49-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ecb49-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="ecb49-138">VirtualNetworkRules 목록</span><span class="sxs-lookup"><span data-stu-id="ecb49-138">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="ecb49-139">-확인</span><span class="sxs-lookup"><span data-stu-id="ecb49-139">-Confirm</span></span>
<span data-ttu-id="ecb49-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb49-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb49-141">-WhatIf</span></span>
<span data-ttu-id="ecb49-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb49-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb49-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb49-144">CommonParameters</span></span>
<span data-ttu-id="ecb49-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb49-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ecb49-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecb49-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb49-147">입력</span><span class="sxs-lookup"><span data-stu-id="ecb49-147">INPUTS</span></span>

### <span data-ttu-id="ecb49-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ecb49-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="ecb49-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ecb49-149">System.String</span></span>

## <span data-ttu-id="ecb49-150">출력</span><span class="sxs-lookup"><span data-stu-id="ecb49-150">OUTPUTS</span></span>

### <span data-ttu-id="ecb49-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ecb49-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ecb49-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecb49-152">NOTES</span></span>

## <span data-ttu-id="ecb49-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb49-153">RELATED LINKS</span></span>