---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 1183ba239ee86f8b587777f26cc3f04154fb5b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993412"
---
# <span data-ttu-id="49970-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="49970-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="49970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49970-102">SYNOPSIS</span></span>
<span data-ttu-id="49970-103">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49970-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="49970-104">구문</span><span class="sxs-lookup"><span data-stu-id="49970-104">SYNTAX</span></span>

### <span data-ttu-id="49970-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="49970-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49970-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="49970-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49970-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49970-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49970-108">설명</span><span class="sxs-lookup"><span data-stu-id="49970-108">DESCRIPTION</span></span>
<span data-ttu-id="49970-109">현재 Azure 구독에서 네임스페이스의 Event Hubs NetworkruleSet의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49970-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="49970-110">예제</span><span class="sxs-lookup"><span data-stu-id="49970-110">EXAMPLES</span></span>

### <span data-ttu-id="49970-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="49970-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="49970-112">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespaces/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="49970-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="49970-113">ResourceGroup 및 네임스페이스 매개 변수를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="49970-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="49970-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="49970-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="49970-115">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespaces/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="49970-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="49970-116">현재 구독에 있는 네임스페이스를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="49970-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="49970-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="49970-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="49970-118">이름 : defaultAction : Id 허용 : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespaces/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="49970-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="49970-119">다른 네임스페이스의 리소스 ID를 사용하여 네임스페이스의 Event Hubs NetworkruleSet에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="49970-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="49970-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49970-120">PARAMETERS</span></span>

### <span data-ttu-id="49970-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49970-121">-DefaultProfile</span></span>
<span data-ttu-id="49970-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49970-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49970-123">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="49970-123">-Namespace</span></span>
<span data-ttu-id="49970-124">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="49970-124">Namespace Name</span></span>

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

### <span data-ttu-id="49970-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49970-125">-ResourceGroupName</span></span>
<span data-ttu-id="49970-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="49970-126">Resource Group Name</span></span>

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

### <span data-ttu-id="49970-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49970-127">-ResourceId</span></span>
<span data-ttu-id="49970-128">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="49970-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="49970-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49970-129">CommonParameters</span></span>
<span data-ttu-id="49970-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49970-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49970-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="49970-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49970-132">입력</span><span class="sxs-lookup"><span data-stu-id="49970-132">INPUTS</span></span>

### <span data-ttu-id="49970-133">System.String</span><span class="sxs-lookup"><span data-stu-id="49970-133">System.String</span></span>

## <span data-ttu-id="49970-134">출력</span><span class="sxs-lookup"><span data-stu-id="49970-134">OUTPUTS</span></span>

### <span data-ttu-id="49970-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="49970-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="49970-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49970-136">NOTES</span></span>

## <span data-ttu-id="49970-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49970-137">RELATED LINKS</span></span>