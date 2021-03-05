---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 339569d3415edadbf284f904358f889e7210267a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015984"
---
# <span data-ttu-id="20987-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="20987-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="20987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20987-102">SYNOPSIS</span></span>
<span data-ttu-id="20987-103">주어진 네임스페이스에 대한 NetworkRuleSet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="20987-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="20987-104">구문</span><span class="sxs-lookup"><span data-stu-id="20987-104">SYNTAX</span></span>

### <span data-ttu-id="20987-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="20987-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20987-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="20987-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20987-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20987-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20987-108">설명</span><span class="sxs-lookup"><span data-stu-id="20987-108">DESCRIPTION</span></span>
<span data-ttu-id="20987-109">주어진 네임스페이스에 대한 NetworkRuleSet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="20987-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="20987-110">예제</span><span class="sxs-lookup"><span data-stu-id="20987-110">EXAMPLES</span></span>

### <span data-ttu-id="20987-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="20987-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="20987-112">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/serviceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="20987-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="20987-113">주어진 "ServiceBus-Namespace1-1375" 네임스페이스에 대한 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20987-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="20987-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="20987-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="20987-115">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="20987-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="20987-116">InputObject를 사용하여 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20987-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="20987-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="20987-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="20987-118">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="20987-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="20987-119">네임스페이스의 ResourceId를 사용하여 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="20987-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="20987-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="20987-120">PARAMETERS</span></span>

### <span data-ttu-id="20987-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20987-121">-AsJob</span></span>
<span data-ttu-id="20987-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="20987-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20987-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20987-123">-DefaultProfile</span></span>
<span data-ttu-id="20987-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20987-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20987-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20987-125">-InputObject</span></span>
<span data-ttu-id="20987-126">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="20987-126">Namespace Object</span></span>

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

### <span data-ttu-id="20987-127">-Name</span><span class="sxs-lookup"><span data-stu-id="20987-127">-Name</span></span>
<span data-ttu-id="20987-128">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="20987-128">Namespace Name</span></span>

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

### <span data-ttu-id="20987-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20987-129">-PassThru</span></span>
<span data-ttu-id="20987-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="20987-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="20987-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20987-131">-ResourceGroupName</span></span>
<span data-ttu-id="20987-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="20987-132">Resource Group Name</span></span>

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

### <span data-ttu-id="20987-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20987-133">-ResourceId</span></span>
<span data-ttu-id="20987-134">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="20987-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="20987-135">-확인</span><span class="sxs-lookup"><span data-stu-id="20987-135">-Confirm</span></span>
<span data-ttu-id="20987-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="20987-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20987-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20987-137">-WhatIf</span></span>
<span data-ttu-id="20987-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="20987-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20987-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20987-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20987-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20987-140">CommonParameters</span></span>
<span data-ttu-id="20987-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20987-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="20987-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="20987-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20987-143">입력</span><span class="sxs-lookup"><span data-stu-id="20987-143">INPUTS</span></span>

### <span data-ttu-id="20987-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="20987-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="20987-145">System.String</span><span class="sxs-lookup"><span data-stu-id="20987-145">System.String</span></span>

## <span data-ttu-id="20987-146">출력</span><span class="sxs-lookup"><span data-stu-id="20987-146">OUTPUTS</span></span>

### <span data-ttu-id="20987-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20987-147">System.Boolean</span></span>

## <span data-ttu-id="20987-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20987-148">NOTES</span></span>

## <span data-ttu-id="20987-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20987-149">RELATED LINKS</span></span>
