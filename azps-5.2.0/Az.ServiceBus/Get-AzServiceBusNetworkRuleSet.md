---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356539"
---
# <span data-ttu-id="26f45-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="26f45-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="26f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f45-102">SYNOPSIS</span></span>
<span data-ttu-id="26f45-103">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="26f45-104">구문</span><span class="sxs-lookup"><span data-stu-id="26f45-104">SYNTAX</span></span>

### <span data-ttu-id="26f45-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="26f45-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26f45-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="26f45-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26f45-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f45-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26f45-108">설명</span><span class="sxs-lookup"><span data-stu-id="26f45-108">DESCRIPTION</span></span>
<span data-ttu-id="26f45-109">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="26f45-110">예제</span><span class="sxs-lookup"><span data-stu-id="26f45-110">EXAMPLES</span></span>

### <span data-ttu-id="26f45-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="26f45-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="26f45-112">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="26f45-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="26f45-113">ResourceGroup 및 네임스페이스 매개 변수를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="26f45-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="26f45-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="26f45-115">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="26f45-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="26f45-116">현재 구독에 있는 네임스페이스를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="26f45-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="26f45-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="26f45-118">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="26f45-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="26f45-119">다른 네임스페이스의 리소스 ID를 사용하여 네임스페이스의 Event Hubs NetworkruleSet 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="26f45-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26f45-120">PARAMETERS</span></span>

### <span data-ttu-id="26f45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f45-121">-DefaultProfile</span></span>
<span data-ttu-id="26f45-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f45-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26f45-123">-Namespace</span></span>
<span data-ttu-id="26f45-124">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="26f45-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f45-125">-ResourceGroupName</span></span>
<span data-ttu-id="26f45-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="26f45-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f45-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26f45-127">-ResourceId</span></span>
<span data-ttu-id="26f45-128">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="26f45-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="26f45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f45-129">CommonParameters</span></span>
<span data-ttu-id="26f45-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26f45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26f45-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="26f45-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f45-132">입력</span><span class="sxs-lookup"><span data-stu-id="26f45-132">INPUTS</span></span>

### <span data-ttu-id="26f45-133">System.String</span><span class="sxs-lookup"><span data-stu-id="26f45-133">System.String</span></span>

## <span data-ttu-id="26f45-134">출력</span><span class="sxs-lookup"><span data-stu-id="26f45-134">OUTPUTS</span></span>

### <span data-ttu-id="26f45-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="26f45-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="26f45-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26f45-136">NOTES</span></span>

## <span data-ttu-id="26f45-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26f45-137">RELATED LINKS</span></span>