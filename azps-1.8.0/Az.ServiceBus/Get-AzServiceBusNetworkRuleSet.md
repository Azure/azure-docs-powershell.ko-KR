---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: d200d342bfa16fb0b2864e0196dc9648b4aa7fcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699202"
---
# <span data-ttu-id="8d162-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8d162-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="8d162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d162-102">SYNOPSIS</span></span>
<span data-ttu-id="8d162-103">현재 Azure 구독에서 네임 스페이스의 이벤트 허브 NetwrokruleSet에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d162-103">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8d162-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d162-104">SYNTAX</span></span>

### <span data-ttu-id="8d162-105">Networkruleset속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d162-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d162-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8d162-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d162-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d162-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d162-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8d162-108">DESCRIPTION</span></span>
<span data-ttu-id="8d162-109">현재 Azure 구독에서 네임 스페이스의 이벤트 허브 NetwrokruleSet에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d162-109">Gets the details of an Event Hubs NetwrokruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="8d162-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8d162-110">EXAMPLES</span></span>

### <span data-ttu-id="8d162-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d162-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="8d162-112">Name: 기본 DefaultAction: 허용 Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 유형: Microsoft ServiceBus/네임 스페이스/네트워크 규칙 집합 IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8d162-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8d162-113">ResourceGroup 및 Namesape 매개 변수를 사용 하 여 네임 스페이스의 이벤트 허브 NetwrokruleSet에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d162-113">Get the details of Event Hubs NetwrokruleSet of namespace using ResourceGroup and Namesape parameters.</span></span> 

### <span data-ttu-id="8d162-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d162-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="8d162-115">Name: 기본 DefaultAction: 허용 Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default 유형: Microsoft ServiceBus/네임 스페이스/네트워크 규칙 집합 IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8d162-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8d162-116">현재 구독에 있는 네임 스페이스를 사용 하 여 네임 스페이스의 이벤트 허브 NetwrokruleSet에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d162-116">Get the details of Event Hubs NetwrokruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="8d162-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="8d162-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="8d162-118">Name: 기본 DefaultAction: 허용 Id:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default 유형: Microsoft ServiceBus/네임 스페이스/네트워크 규칙 집합 IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="8d162-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="8d162-119">다른 네임 스페이스의 리소스 Id를 사용 하 여 네임 스페이스의 이벤트 허브 NetwrokruleSet에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d162-119">Get the details of Event Hubs NetwrokruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="8d162-120">변수</span><span class="sxs-lookup"><span data-stu-id="8d162-120">PARAMETERS</span></span>

### <span data-ttu-id="8d162-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d162-121">-DefaultProfile</span></span>
<span data-ttu-id="8d162-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d162-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d162-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8d162-123">-Namespace</span></span>
<span data-ttu-id="8d162-124">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="8d162-124">Namespace Name</span></span>

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

### <span data-ttu-id="8d162-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d162-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d162-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8d162-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8d162-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d162-127">-ResourceId</span></span>
<span data-ttu-id="8d162-128">네임 스페이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8d162-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8d162-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d162-129">CommonParameters</span></span>
<span data-ttu-id="8d162-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d162-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8d162-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d162-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d162-132">입력</span><span class="sxs-lookup"><span data-stu-id="8d162-132">INPUTS</span></span>

### <span data-ttu-id="8d162-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d162-133">System.String</span></span>

## <span data-ttu-id="8d162-134">출력</span><span class="sxs-lookup"><span data-stu-id="8d162-134">OUTPUTS</span></span>

### <span data-ttu-id="8d162-135">ServiceBus를 호출 합니다. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="8d162-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="8d162-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8d162-136">NOTES</span></span>

## <span data-ttu-id="8d162-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d162-137">RELATED LINKS</span></span>