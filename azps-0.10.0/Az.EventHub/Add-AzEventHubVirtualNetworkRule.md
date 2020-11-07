---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 37f13534095341895a4fc3b4c1c9feb9e5e911be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875947"
---
# <span data-ttu-id="632c7-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="632c7-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="632c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="632c7-102">SYNOPSIS</span></span>
<span data-ttu-id="632c7-103">지정 된 네임 스페이스에 대 한 단일 VirtualNetworkRule를 네트워크 규칙 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="632c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="632c7-104">SYNTAX</span></span>

### <span data-ttu-id="632c7-105">VirtualNetworkRulePropertiesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="632c7-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="632c7-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="632c7-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="632c7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="632c7-107">DESCRIPTION</span></span>
<span data-ttu-id="632c7-108">지정 된 네임 스페이스에 대 한 단일 VirtualNetworkRule를 네트워크 규칙 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="632c7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="632c7-109">EXAMPLES</span></span>

### <span data-ttu-id="632c7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="632c7-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="632c7-111">Name: 기본 DefaultAction: Allow Id:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="632c7-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="632c7-112">주어진 서브넷 및 IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule)를 지정 된 네임 스페이스에 대 한 네트워크 규칙 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="632c7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="632c7-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="632c7-114">Name: 기본 DefaultAction: Allow Id:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="632c7-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="632c7-115">지정 된 네임 스페이스에 대 한 $virtualruleset 1의 NetworkRuleSet 집합을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="632c7-116">변수</span><span class="sxs-lookup"><span data-stu-id="632c7-116">PARAMETERS</span></span>

### <span data-ttu-id="632c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632c7-117">-DefaultProfile</span></span>
<span data-ttu-id="632c7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="632c7-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="632c7-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="632c7-120">서브넷의 팔 ID</span><span class="sxs-lookup"><span data-stu-id="632c7-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="632c7-121">-이름</span><span class="sxs-lookup"><span data-stu-id="632c7-121">-Name</span></span>
<span data-ttu-id="632c7-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="632c7-122">Namespace Name</span></span>

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

### <span data-ttu-id="632c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="632c7-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="632c7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="632c7-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="632c7-125">-SubnetId</span></span>
<span data-ttu-id="632c7-126">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="632c7-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="632c7-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="632c7-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="632c7-128">VirtualNetworkRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="632c7-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="632c7-129">-확인</span><span class="sxs-lookup"><span data-stu-id="632c7-129">-Confirm</span></span>
<span data-ttu-id="632c7-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="632c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="632c7-131">-WhatIf</span></span>
<span data-ttu-id="632c7-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="632c7-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="632c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632c7-134">CommonParameters</span></span>
<span data-ttu-id="632c7-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="632c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="632c7-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632c7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632c7-137">입력</span><span class="sxs-lookup"><span data-stu-id="632c7-137">INPUTS</span></span>

### <span data-ttu-id="632c7-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="632c7-138">System.String</span></span>

### <span data-ttu-id="632c7-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="632c7-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="632c7-140">PSNWRuleSetVirtualNetworkRulesAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="632c7-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="632c7-141">출력</span><span class="sxs-lookup"><span data-stu-id="632c7-141">OUTPUTS</span></span>

### <span data-ttu-id="632c7-142">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="632c7-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="632c7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="632c7-143">NOTES</span></span>

## <span data-ttu-id="632c7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="632c7-144">RELATED LINKS</span></span>
