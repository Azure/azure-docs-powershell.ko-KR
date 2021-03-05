---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 6b01211b7efa20983f868c7e70e54be02d5ad5c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001563"
---
# <span data-ttu-id="77018-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="77018-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="77018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77018-102">SYNOPSIS</span></span>
<span data-ttu-id="77018-103">주어진 네임스페이스의 NetworkRuleSet에 단일 IP 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="77018-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="77018-104">구문</span><span class="sxs-lookup"><span data-stu-id="77018-104">SYNTAX</span></span>

### <span data-ttu-id="77018-105">IPRulePropertiesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="77018-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77018-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77018-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77018-107">설명</span><span class="sxs-lookup"><span data-stu-id="77018-107">DESCRIPTION</span></span>
<span data-ttu-id="77018-108">주어진 네임스페이스의 NetworkRuleSet에 단일 IP 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="77018-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="77018-109">예제</span><span class="sxs-lookup"><span data-stu-id="77018-109">EXAMPLES</span></span>

### <span data-ttu-id="77018-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="77018-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="77018-111">이름 : defaultAction : Id 허용 : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/eventhub-Namespaces/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.4, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="77018-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="77018-112">IPMask "11.22.33.44"와 주어진 네임스페이스에 대한 작업 허용을 사용하여 IPRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="77018-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="77018-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="77018-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="77018-114">이름 : defaultAction : Id 허용 : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/eventhub-Namespaces/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.4, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="77018-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="77018-115">IPMask "11.22.33.44"와 주어진 네임스페이스에 대한 작업 허용을 사용하여 IPRule을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="77018-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="77018-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="77018-116">PARAMETERS</span></span>

### <span data-ttu-id="77018-117">-Action</span><span class="sxs-lookup"><span data-stu-id="77018-117">-Action</span></span>
<span data-ttu-id="77018-118">IP 필터 작업</span><span class="sxs-lookup"><span data-stu-id="77018-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77018-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77018-119">-DefaultProfile</span></span>
<span data-ttu-id="77018-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77018-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77018-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="77018-121">-IpMask</span></span>
<span data-ttu-id="77018-122">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="77018-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77018-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="77018-123">-IpRuleObject</span></span>
<span data-ttu-id="77018-124">추가할 IPRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="77018-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77018-125">-Name</span><span class="sxs-lookup"><span data-stu-id="77018-125">-Name</span></span>
<span data-ttu-id="77018-126">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="77018-126">Namespace Name</span></span>

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

### <span data-ttu-id="77018-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77018-127">-ResourceGroupName</span></span>
<span data-ttu-id="77018-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="77018-128">Resource Group Name</span></span>

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

### <span data-ttu-id="77018-129">-확인</span><span class="sxs-lookup"><span data-stu-id="77018-129">-Confirm</span></span>
<span data-ttu-id="77018-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="77018-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77018-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77018-131">-WhatIf</span></span>
<span data-ttu-id="77018-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="77018-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77018-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77018-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77018-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77018-134">CommonParameters</span></span>
<span data-ttu-id="77018-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77018-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77018-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="77018-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77018-137">입력</span><span class="sxs-lookup"><span data-stu-id="77018-137">INPUTS</span></span>

### <span data-ttu-id="77018-138">System.String</span><span class="sxs-lookup"><span data-stu-id="77018-138">System.String</span></span>

### <span data-ttu-id="77018-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="77018-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="77018-140">출력</span><span class="sxs-lookup"><span data-stu-id="77018-140">OUTPUTS</span></span>

### <span data-ttu-id="77018-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="77018-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="77018-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77018-142">NOTES</span></span>

## <span data-ttu-id="77018-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77018-143">RELATED LINKS</span></span>
