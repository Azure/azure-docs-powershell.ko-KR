---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042865"
---
# <span data-ttu-id="b8245-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="b8245-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="b8245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8245-102">SYNOPSIS</span></span>
<span data-ttu-id="b8245-103">지정 된 네임 스페이스의 NetworkRuleSet에 단일 IP 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="b8245-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b8245-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8245-104">SYNTAX</span></span>

### <span data-ttu-id="b8245-105">IPRulePropertiesParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8245-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8245-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8245-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8245-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8245-107">DESCRIPTION</span></span>
<span data-ttu-id="b8245-108">지정 된 네임 스페이스의 NetworkRuleSet에 단일 IP 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="b8245-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="b8245-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8245-109">EXAMPLES</span></span>

### <span data-ttu-id="b8245-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8245-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="b8245-111">Name: 기본 DefaultAction: Allow Id:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/네임 스페이스/NetworkRuleSet 집합 IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="b8245-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b8245-112">IpMask "11.22.33.44"를 사용 하 여 IPRule를 추가 하 고 지정 된 네임 스페이스에 대해 작업을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="b8245-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8245-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="b8245-114">Name: 기본 DefaultAction: Allow Id:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/네임 스페이스/NetworkRuleSet 집합 IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="b8245-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="b8245-115">IpMask "11.22.33.44"를 사용 하 여 IPRule를 추가 하 고 지정 된 네임 스페이스에 대해 작업을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="b8245-116">변수</span><span class="sxs-lookup"><span data-stu-id="b8245-116">PARAMETERS</span></span>

### <span data-ttu-id="b8245-117">-작업</span><span class="sxs-lookup"><span data-stu-id="b8245-117">-Action</span></span>
<span data-ttu-id="b8245-118">IP 필터 동작</span><span class="sxs-lookup"><span data-stu-id="b8245-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="b8245-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8245-119">-DefaultProfile</span></span>
<span data-ttu-id="b8245-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8245-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="b8245-121">-IpMask</span></span>
<span data-ttu-id="b8245-122">서브넷 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b8245-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="b8245-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="b8245-123">-IpRuleObject</span></span>
<span data-ttu-id="b8245-124">IPRule 구성 개체를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="b8245-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b8245-125">-Name</span></span>
<span data-ttu-id="b8245-126">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b8245-126">Namespace Name</span></span>

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

### <span data-ttu-id="b8245-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8245-127">-ResourceGroupName</span></span>
<span data-ttu-id="b8245-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b8245-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b8245-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b8245-129">-Confirm</span></span>
<span data-ttu-id="b8245-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8245-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8245-131">-WhatIf</span></span>
<span data-ttu-id="b8245-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8245-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8245-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8245-134">CommonParameters</span></span>
<span data-ttu-id="b8245-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8245-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b8245-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8245-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8245-137">입력</span><span class="sxs-lookup"><span data-stu-id="b8245-137">INPUTS</span></span>

### <span data-ttu-id="b8245-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8245-138">System.String</span></span>

### <span data-ttu-id="b8245-139">PSNWRuleSetIpRulesAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="b8245-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="b8245-140">출력</span><span class="sxs-lookup"><span data-stu-id="b8245-140">OUTPUTS</span></span>

### <span data-ttu-id="b8245-141">Microsoft. \*. a. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="b8245-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="b8245-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b8245-142">NOTES</span></span>

## <span data-ttu-id="b8245-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8245-143">RELATED LINKS</span></span>
