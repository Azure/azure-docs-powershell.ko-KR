---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214962"
---
# <span data-ttu-id="dd2ba-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd2ba-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="dd2ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2ba-103">지정 된 네임 스페이스에 대 한 네트워크 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="dd2ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd2ba-104">SYNTAX</span></span>

### <span data-ttu-id="dd2ba-105">Networkruleset속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="dd2ba-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd2ba-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd2ba-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd2ba-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd2ba-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2ba-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dd2ba-108">DESCRIPTION</span></span>
<span data-ttu-id="dd2ba-109">지정 된 네임 스페이스에 대 한 네트워크 규칙 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="dd2ba-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dd2ba-110">EXAMPLES</span></span>

### <span data-ttu-id="dd2ba-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd2ba-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="dd2ba-112">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dd2ba-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="dd2ba-113">지정 된 "Eventhub-Namespace1-1375" 네임 스페이스에 대 한 NetworkRuleSet를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="dd2ba-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="dd2ba-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="dd2ba-115">InputObject를 사용 하 여 NetworkRuleSet 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="dd2ba-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="dd2ba-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="dd2ba-117">Name: 기본 DefaultAction: Allow Id:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/네임 스페이스/NetworkRuleSet 집합 IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dd2ba-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="dd2ba-118">네임 스페이스 ResourceId를 사용 하 여 네트워크 규칙 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="dd2ba-119">변수</span><span class="sxs-lookup"><span data-stu-id="dd2ba-119">PARAMETERS</span></span>

### <span data-ttu-id="dd2ba-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd2ba-120">-AsJob</span></span>
<span data-ttu-id="dd2ba-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dd2ba-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2ba-122">-DefaultProfile</span></span>
<span data-ttu-id="dd2ba-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2ba-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd2ba-124">-InputObject</span></span>
<span data-ttu-id="dd2ba-125">네임 스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="dd2ba-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2ba-126">-이름</span><span class="sxs-lookup"><span data-stu-id="dd2ba-126">-Name</span></span>
<span data-ttu-id="dd2ba-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="dd2ba-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2ba-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd2ba-128">-PassThru</span></span>
<span data-ttu-id="dd2ba-129">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="dd2ba-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2ba-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2ba-130">-ResourceGroupName</span></span>
<span data-ttu-id="dd2ba-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dd2ba-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2ba-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2ba-132">-ResourceId</span></span>
<span data-ttu-id="dd2ba-133">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="dd2ba-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2ba-134">-확인</span><span class="sxs-lookup"><span data-stu-id="dd2ba-134">-Confirm</span></span>
<span data-ttu-id="dd2ba-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2ba-136">-WhatIf</span></span>
<span data-ttu-id="dd2ba-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2ba-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2ba-139">CommonParameters</span></span>
<span data-ttu-id="dd2ba-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd2ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dd2ba-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2ba-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2ba-142">입력</span><span class="sxs-lookup"><span data-stu-id="dd2ba-142">INPUTS</span></span>

### <span data-ttu-id="dd2ba-143">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="dd2ba-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="dd2ba-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd2ba-144">System.String</span></span>

## <span data-ttu-id="dd2ba-145">출력</span><span class="sxs-lookup"><span data-stu-id="dd2ba-145">OUTPUTS</span></span>

### <span data-ttu-id="dd2ba-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dd2ba-146">System.Boolean</span></span>

## <span data-ttu-id="dd2ba-147">상속자</span><span class="sxs-lookup"><span data-stu-id="dd2ba-147">NOTES</span></span>

## <span data-ttu-id="dd2ba-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd2ba-148">RELATED LINKS</span></span>