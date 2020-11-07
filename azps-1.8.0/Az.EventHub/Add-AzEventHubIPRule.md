---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 959fcab661139a1cacae46a315db0eaa93f0c09e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700859"
---
# <span data-ttu-id="0b12c-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="0b12c-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="0b12c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b12c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b12c-103">지정 된 네임 스페이스의 네트워크 규칙 집합에 단일 IPrule 추가</span><span class="sxs-lookup"><span data-stu-id="0b12c-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="0b12c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b12c-104">SYNTAX</span></span>

### <span data-ttu-id="0b12c-105">IPRulePropertiesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0b12c-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b12c-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b12c-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b12c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0b12c-107">DESCRIPTION</span></span>
<span data-ttu-id="0b12c-108">지정 된 네임 스페이스의 네트워크 규칙 집합에 단일 IPrule 추가</span><span class="sxs-lookup"><span data-stu-id="0b12c-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="0b12c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0b12c-109">EXAMPLES</span></span>

### <span data-ttu-id="0b12c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b12c-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="0b12c-111">Name: 기본 DefaultAction: Allow Id:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/네임 스페이스/NetworkRuleSet 집합 IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="0b12c-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="0b12c-112">IpMask "11.22.33.44"를 사용 하 여 IPRule를 추가 하 고 지정 된 namesapce에 대해 작업을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

### <span data-ttu-id="0b12c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0b12c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="0b12c-114">Name: 기본 DefaultAction: Allow Id:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/네임 스페이스/NetworkRuleSet 집합 IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="0b12c-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="0b12c-115">IpMask "11.22.33.44"를 사용 하 여 IPRule를 추가 하 고 지정 된 namesapce에 대해 작업을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

## <span data-ttu-id="0b12c-116">변수</span><span class="sxs-lookup"><span data-stu-id="0b12c-116">PARAMETERS</span></span>

### <span data-ttu-id="0b12c-117">-작업</span><span class="sxs-lookup"><span data-stu-id="0b12c-117">-Action</span></span>
<span data-ttu-id="0b12c-118">IP 필터 동작</span><span class="sxs-lookup"><span data-stu-id="0b12c-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="0b12c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b12c-119">-DefaultProfile</span></span>
<span data-ttu-id="0b12c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b12c-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="0b12c-121">-IpMask</span></span>
<span data-ttu-id="0b12c-122">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0b12c-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="0b12c-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="0b12c-123">-IpRuleObject</span></span>
<span data-ttu-id="0b12c-124">IPRule 구성 개체를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="0b12c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="0b12c-125">-Name</span></span>
<span data-ttu-id="0b12c-126">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="0b12c-126">Namespace Name</span></span>

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

### <span data-ttu-id="0b12c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b12c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b12c-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0b12c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="0b12c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="0b12c-129">-Confirm</span></span>
<span data-ttu-id="0b12c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b12c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b12c-131">-WhatIf</span></span>
<span data-ttu-id="0b12c-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b12c-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b12c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b12c-134">CommonParameters</span></span>
<span data-ttu-id="0b12c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b12c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0b12c-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b12c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b12c-137">입력</span><span class="sxs-lookup"><span data-stu-id="0b12c-137">INPUTS</span></span>

### <span data-ttu-id="0b12c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b12c-138">System.String</span></span>

### <span data-ttu-id="0b12c-139">PSNWRuleSetIpRulesAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="0b12c-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="0b12c-140">출력</span><span class="sxs-lookup"><span data-stu-id="0b12c-140">OUTPUTS</span></span>

### <span data-ttu-id="0b12c-141">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="0b12c-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="0b12c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="0b12c-142">NOTES</span></span>

## <span data-ttu-id="0b12c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b12c-143">RELATED LINKS</span></span>
