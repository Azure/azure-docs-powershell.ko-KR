---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 8fa4589225d9427db5a3aee4b9fc49f1a1294138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877786"
---
# <span data-ttu-id="28426-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="28426-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="28426-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28426-102">SYNOPSIS</span></span>
<span data-ttu-id="28426-103">현재 Azure 구독에서 지정 된 네임 스페이스의 NetworkruleSet 규칙 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28426-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="28426-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28426-104">SYNTAX</span></span>

### <span data-ttu-id="28426-105">Networkruleset속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="28426-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28426-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28426-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28426-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28426-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28426-108">설명은</span><span class="sxs-lookup"><span data-stu-id="28426-108">DESCRIPTION</span></span>
<span data-ttu-id="28426-109">현재 Azure 구독에서 지정 된 네임 스페이스의 NetworkruleSet 규칙 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28426-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="28426-110">예제의</span><span class="sxs-lookup"><span data-stu-id="28426-110">EXAMPLES</span></span>

### <span data-ttu-id="28426-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="28426-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="28426-112">Name: 기본 DefaultAction: 허용 Id:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft IpRules: EventHub/네임 스페이스/네트워크 규칙 집합-4.4.4.4, 허용, 3.3.3.3, 허용} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="28426-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="28426-113">-IPRule 및-VirtualNetworkRule 매개 변수를 사용 하 여 네트워크 규칙 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="28426-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="28426-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="28426-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="28426-115">Name: 기본 DefaultAction: 허용 Id:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft IpRules: EventHub/네임 스페이스/네트워크 규칙 집합-4.4.4.4, 허용, 3.3.3.3, 허용} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="28426-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="28426-116">-InputObject를 사용 하 여 NetworkRuleSet 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="28426-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="28426-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="28426-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="28426-118">Name: 기본 DefaultAction: 허용 Id:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft IpRules: EventHub/네임 스페이스/네트워크 규칙 집합-4.4.4.4, 허용, 3.3.3.3, 허용} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="28426-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="28426-119">다른 네임 스페이스의-ResourceId를 사용 하 여 NetworkRuleSet 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28426-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="28426-120">변수</span><span class="sxs-lookup"><span data-stu-id="28426-120">PARAMETERS</span></span>

### <span data-ttu-id="28426-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="28426-121">-DefaultAction</span></span>
<span data-ttu-id="28426-122">NetworkRuleSet 집합에 대 한 기본 작업</span><span class="sxs-lookup"><span data-stu-id="28426-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="28426-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28426-123">-DefaultProfile</span></span>
<span data-ttu-id="28426-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28426-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28426-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28426-125">-InputObject</span></span>
<span data-ttu-id="28426-126">NetworkruleSet 집합 구성 개체</span><span class="sxs-lookup"><span data-stu-id="28426-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="28426-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="28426-127">-IPRule</span></span>
<span data-ttu-id="28426-128">IPRuleSet 목록</span><span class="sxs-lookup"><span data-stu-id="28426-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="28426-129">-이름</span><span class="sxs-lookup"><span data-stu-id="28426-129">-Name</span></span>
<span data-ttu-id="28426-130">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28426-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="28426-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28426-131">-ResourceGroupName</span></span>
<span data-ttu-id="28426-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28426-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="28426-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28426-133">-ResourceId</span></span>
<span data-ttu-id="28426-134">네임 스페이스의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="28426-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="28426-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="28426-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="28426-136">VirtualNetworkRules 목록</span><span class="sxs-lookup"><span data-stu-id="28426-136">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="28426-137">-확인</span><span class="sxs-lookup"><span data-stu-id="28426-137">-Confirm</span></span>
<span data-ttu-id="28426-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28426-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28426-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28426-139">-WhatIf</span></span>
<span data-ttu-id="28426-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28426-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28426-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28426-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28426-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28426-142">CommonParameters</span></span>
<span data-ttu-id="28426-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28426-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="28426-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28426-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28426-145">입력</span><span class="sxs-lookup"><span data-stu-id="28426-145">INPUTS</span></span>

### <span data-ttu-id="28426-146">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="28426-146">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="28426-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28426-147">System.String</span></span>

## <span data-ttu-id="28426-148">출력</span><span class="sxs-lookup"><span data-stu-id="28426-148">OUTPUTS</span></span>

### <span data-ttu-id="28426-149">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="28426-149">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="28426-150">상속자</span><span class="sxs-lookup"><span data-stu-id="28426-150">NOTES</span></span>

## <span data-ttu-id="28426-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28426-151">RELATED LINKS</span></span>