---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337274"
---
# <span data-ttu-id="3039b-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="3039b-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="3039b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3039b-102">SYNOPSIS</span></span>
<span data-ttu-id="3039b-103">주어진 네임스페이스의 NetworkRuleSet에 단일 IP 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="3039b-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3039b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3039b-104">SYNTAX</span></span>

### <span data-ttu-id="3039b-105">IPRulePropertiesParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3039b-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3039b-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3039b-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3039b-107">설명</span><span class="sxs-lookup"><span data-stu-id="3039b-107">DESCRIPTION</span></span>
<span data-ttu-id="3039b-108">주어진 네임스페이스의 NetworkRuleSet에 단일 IP 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="3039b-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3039b-109">예제</span><span class="sxs-lookup"><span data-stu-id="3039b-109">EXAMPLES</span></span>

### <span data-ttu-id="3039b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3039b-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="3039b-111">이름 : defaultAction : 허용 ID : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="3039b-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="3039b-112">IpMask "11.22.33.44"를 사용하여 IPRule을 추가하고 작업 허용을 제공된 네임스페이스에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3039b-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="3039b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3039b-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="3039b-114">이름 : defaultAction : 허용 ID : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="3039b-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="3039b-115">IpMask "11.22.33.44"를 사용하여 IPRule을 추가하고 작업 허용을 제공된 네임스페이스에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3039b-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="3039b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3039b-116">PARAMETERS</span></span>

### <span data-ttu-id="3039b-117">-Action</span><span class="sxs-lookup"><span data-stu-id="3039b-117">-Action</span></span>
<span data-ttu-id="3039b-118">IP 필터 작업</span><span class="sxs-lookup"><span data-stu-id="3039b-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="3039b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3039b-119">-DefaultProfile</span></span>
<span data-ttu-id="3039b-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3039b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3039b-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="3039b-121">-IpMask</span></span>
<span data-ttu-id="3039b-122">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="3039b-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="3039b-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3039b-123">-IpRuleObject</span></span>
<span data-ttu-id="3039b-124">추가할 IPRule 구성 개체</span><span class="sxs-lookup"><span data-stu-id="3039b-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3039b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3039b-125">-Name</span></span>
<span data-ttu-id="3039b-126">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3039b-126">Namespace Name</span></span>

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

### <span data-ttu-id="3039b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3039b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3039b-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3039b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="3039b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3039b-129">-Confirm</span></span>
<span data-ttu-id="3039b-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3039b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3039b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3039b-131">-WhatIf</span></span>
<span data-ttu-id="3039b-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3039b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3039b-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3039b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3039b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3039b-134">CommonParameters</span></span>
<span data-ttu-id="3039b-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3039b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3039b-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3039b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3039b-137">입력</span><span class="sxs-lookup"><span data-stu-id="3039b-137">INPUTS</span></span>

### <span data-ttu-id="3039b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3039b-138">System.String</span></span>

### <span data-ttu-id="3039b-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3039b-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="3039b-140">출력</span><span class="sxs-lookup"><span data-stu-id="3039b-140">OUTPUTS</span></span>

### <span data-ttu-id="3039b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="3039b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="3039b-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3039b-142">NOTES</span></span>

## <span data-ttu-id="3039b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3039b-143">RELATED LINKS</span></span>