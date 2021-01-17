---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332606"
---
# <span data-ttu-id="07b0f-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="07b0f-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="07b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="07b0f-103">주어진 네임스페이스에 대한 NetworkRuleSet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="07b0f-104">구문</span><span class="sxs-lookup"><span data-stu-id="07b0f-104">SYNTAX</span></span>

### <span data-ttu-id="07b0f-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="07b0f-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b0f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="07b0f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b0f-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07b0f-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07b0f-108">설명</span><span class="sxs-lookup"><span data-stu-id="07b0f-108">DESCRIPTION</span></span>
<span data-ttu-id="07b0f-109">주어진 네임스페이스에 대한 NetworkRuleSet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="07b0f-110">예제</span><span class="sxs-lookup"><span data-stu-id="07b0f-110">EXAMPLES</span></span>

### <span data-ttu-id="07b0f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="07b0f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="07b0f-112">이름: defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="07b0f-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="07b0f-113">주어진 "ServiceBus-Namespace1-1375" 네임스페이스에 대한 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="07b0f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="07b0f-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="07b0f-115">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="07b0f-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="07b0f-116">InputObject를 사용하여 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="07b0f-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="07b0f-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="07b0f-118">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="07b0f-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="07b0f-119">네임스페이스의 ResourceId를 사용하여 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="07b0f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07b0f-120">PARAMETERS</span></span>

### <span data-ttu-id="07b0f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07b0f-121">-AsJob</span></span>
<span data-ttu-id="07b0f-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="07b0f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07b0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b0f-123">-DefaultProfile</span></span>
<span data-ttu-id="07b0f-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b0f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07b0f-125">-InputObject</span></span>
<span data-ttu-id="07b0f-126">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="07b0f-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07b0f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="07b0f-127">-Name</span></span>
<span data-ttu-id="07b0f-128">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="07b0f-128">Namespace Name</span></span>

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

### <span data-ttu-id="07b0f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07b0f-129">-PassThru</span></span>
<span data-ttu-id="07b0f-130">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="07b0f-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="07b0f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b0f-131">-ResourceGroupName</span></span>
<span data-ttu-id="07b0f-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="07b0f-132">Resource Group Name</span></span>

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

### <span data-ttu-id="07b0f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07b0f-133">-ResourceId</span></span>
<span data-ttu-id="07b0f-134">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07b0f-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="07b0f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07b0f-135">-Confirm</span></span>
<span data-ttu-id="07b0f-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b0f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b0f-137">-WhatIf</span></span>
<span data-ttu-id="07b0f-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="07b0f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b0f-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b0f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b0f-140">CommonParameters</span></span>
<span data-ttu-id="07b0f-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07b0f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="07b0f-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07b0f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b0f-143">입력</span><span class="sxs-lookup"><span data-stu-id="07b0f-143">INPUTS</span></span>

### <span data-ttu-id="07b0f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="07b0f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="07b0f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="07b0f-145">System.String</span></span>

## <span data-ttu-id="07b0f-146">출력</span><span class="sxs-lookup"><span data-stu-id="07b0f-146">OUTPUTS</span></span>

### <span data-ttu-id="07b0f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07b0f-147">System.Boolean</span></span>

## <span data-ttu-id="07b0f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07b0f-148">NOTES</span></span>

## <span data-ttu-id="07b0f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07b0f-149">RELATED LINKS</span></span>
