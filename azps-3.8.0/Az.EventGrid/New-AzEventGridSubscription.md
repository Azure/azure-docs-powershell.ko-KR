---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1e2ac4d8763376da6854b3c5d1551e4213f25f60
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395308"
---
# <span data-ttu-id="21ef0-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="21ef0-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="21ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="21ef0-103">항목, Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 Azure 이벤트 그리드 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="21ef0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21ef0-104">SYNTAX</span></span>

### <span data-ttu-id="21ef0-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="21ef0-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ef0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ef0-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ef0-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ef0-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ef0-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21ef0-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21ef0-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ef0-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21ef0-113">설명은</span><span class="sxs-lookup"><span data-stu-id="21ef0-113">DESCRIPTION</span></span>
<span data-ttu-id="21ef0-114">Azure 이벤트 그리드 항목, 지원 되는 Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="21ef0-115">현재 선택 된 Azure 구독에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="21ef0-116">리소스 그룹에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점 외에도 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="21ef0-117">Azure 이벤트 그리드 항목에 대 한 이벤트 구독을 만들려면 항목 이름도 함께 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="21ef0-118">지원 되는 Azure 리소스에 대 한 이벤트 구독을 만들려면 리소스의 전체 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="21ef0-119">지원 되는 형식 목록을 보려면 Get-AzEventGridTopicType cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="21ef0-120">예제의</span><span class="sxs-lookup"><span data-stu-id="21ef0-120">EXAMPLES</span></span>

### <span data-ttu-id="21ef0-121">예제 1</span><span class="sxs-lookup"><span data-stu-id="21ef0-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="21ef0-122">\` \` \` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName에서 Azure 이벤트 그리드 항목 Topic1에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="21ef0-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="21ef0-123">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="21ef0-124">예제 2</span><span class="sxs-lookup"><span data-stu-id="21ef0-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="21ef0-125">\` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="21ef0-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="21ef0-126">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="21ef0-127">예제 3</span><span class="sxs-lookup"><span data-stu-id="21ef0-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="21ef0-128">\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="21ef0-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="21ef0-129">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="21ef0-130">예제 4</span><span class="sxs-lookup"><span data-stu-id="21ef0-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="21ef0-131">\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="21ef0-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="21ef0-132">이 이벤트 구독은 이벤트 유형 및 주체의 추가 필터를 지정 하 고 해당 필터와 일치 하는 이벤트만 대상 끝점에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="21ef0-133">예제 5</span><span class="sxs-lookup"><span data-stu-id="21ef0-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="21ef0-134">\` \` 지정 된 이벤트 허브가 있는 현재 선택한 Azure 구독에 대 한 EventSubscription1 이벤트의 대상으로 새 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="21ef0-135">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="21ef0-136">예제 6</span><span class="sxs-lookup"><span data-stu-id="21ef0-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="21ef0-137">\` \` 지정 된 webhook 대상 끝점을 사용 하 여 EventHub 네임 스페이스에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="21ef0-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="21ef0-138">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="21ef0-139">변수</span><span class="sxs-lookup"><span data-stu-id="21ef0-139">PARAMETERS</span></span>

### <span data-ttu-id="21ef0-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="21ef0-140">-AdvancedFilter</span></span>
<span data-ttu-id="21ef0-141">특성 기반 필터링에 사용 되는 여러 해시 테이블 값의 배열을 지정 하는 고급 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="21ef0-142">각 해시 테이블 값에는 작업, 키, 값 또는 값의 키 값 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="21ef0-143">Operator는 번호 In, 숫자 Notin, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, Stringin 또는 Stringin 값 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="21ef0-144">Key는 고급 필터링 정책이 적용 되는 페이로드 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="21ef0-145">마지막으로 값 또는 값은 일치 시킬 값 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="21ef0-146">해당 형식 또는 값의 배열에 대 한 단일 값이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="21ef0-147">고급 필터 매개 변수의 예: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) $AdvFilter 1 = @ {연산자 = "숫자 In", key = "Data. Key1"; 값 = @ (1, 2)} 및 $AdvFilter 2 = @ {operator = "StringBringsWith"; key = "Subject"; 값 = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="21ef0-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="21ef0-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="21ef0-149">배달 되지 않은 이벤트를 저장 하는 데 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="21ef0-150">저장소 blob 컨테이너의 Azure 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="21ef0-151">예:/subscriptions/[SubscriptionId]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="21ef0-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ef0-152">-DefaultProfile</span></span>
<span data-ttu-id="21ef0-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="21ef0-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ef0-154">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="21ef0-154">-DomainInputObject</span></span>
<span data-ttu-id="21ef0-155">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="21ef0-155">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-156">-DomainName</span><span class="sxs-lookup"><span data-stu-id="21ef0-156">-DomainName</span></span>
<span data-ttu-id="21ef0-157">이벤트 구독을 만들어야 하는 이벤트 그리드 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="21ef0-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="21ef0-159">EventGrid 도메인 주제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-159">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="21ef0-160">-DomainTopicName</span></span>
<span data-ttu-id="21ef0-161">이벤트 구독을 만들어야 하는 도메인 항목의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-162">-끝점</span><span class="sxs-lookup"><span data-stu-id="21ef0-162">-Endpoint</span></span>
<span data-ttu-id="21ef0-163">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="21ef0-164">이는 webhook URL 또는 EventHub, storage queue, hybridconnection 또는 servicebusqueue의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="21ef0-165">예를 들어 하이브리드 연결의 리소스 ID에는/subscriptions/[Azure 구독 ID]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName] 형식이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="21ef0-166">이벤트 그리드 cmdlet을 실행 하기 전에 대상 끝점을 만들어 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="21ef0-167">-EndpointType</span></span>
<span data-ttu-id="21ef0-168">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-168">Endpoint Type.</span></span>
<span data-ttu-id="21ef0-169">이는 webhook, eventhub, storagequeue, hybridconnection 또는 servicebusqueue 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="21ef0-170">기본값은 webhook입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="21ef0-171">-EventSubscriptionName</span></span>
<span data-ttu-id="21ef0-172">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-172">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="21ef0-173">-EventTtl</span></span>
<span data-ttu-id="21ef0-174">이벤트 배달을 위한 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="21ef0-175">이 값은 1에서 1440 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-176">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="21ef0-176">-ExpirationDate</span></span>
<span data-ttu-id="21ef0-177">이벤트 구독이 중지 될 때 이벤트 구독에 대 한 만료 날짜/시간을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="21ef0-178">-IncludedEventType</span></span>
<span data-ttu-id="21ef0-179">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21ef0-180">-InputObject</span></span>
<span data-ttu-id="21ef0-181">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="21ef0-181">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-182">-레이블</span><span class="sxs-lookup"><span data-stu-id="21ef0-182">-Label</span></span>
<span data-ttu-id="21ef0-183">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="21ef0-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-184">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="21ef0-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="21ef0-185">이벤트 배달을 위한 최대 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="21ef0-186">이 값은 1에서 30 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ef0-187">-ResourceGroupName</span></span>
<span data-ttu-id="21ef0-188">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-188">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-189">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21ef0-189">-ResourceId</span></span>
<span data-ttu-id="21ef0-190">이벤트 구독을 만들어야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-190">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="21ef0-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="21ef0-192">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="21ef0-193">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-194">-이란 Casesensitive</span><span class="sxs-lookup"><span data-stu-id="21ef0-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="21ef0-195">주제 필드가 대/소문자를 구분 하 여 비교 하도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="21ef0-196">지정 하지 않으면 제목은 대/소문자를 구분 하지 않고 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="21ef0-197">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="21ef0-197">-SubjectEndsWith</span></span>
<span data-ttu-id="21ef0-198">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="21ef0-199">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-200">-TopicName</span><span class="sxs-lookup"><span data-stu-id="21ef0-200">-TopicName</span></span>
<span data-ttu-id="21ef0-201">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-201">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ef0-202">-확인</span><span class="sxs-lookup"><span data-stu-id="21ef0-202">-Confirm</span></span>
<span data-ttu-id="21ef0-203">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ef0-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ef0-204">-WhatIf</span></span>
<span data-ttu-id="21ef0-205">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ef0-206">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ef0-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ef0-207">CommonParameters</span></span>
<span data-ttu-id="21ef0-208">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21ef0-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ef0-209">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ef0-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ef0-210">입력</span><span class="sxs-lookup"><span data-stu-id="21ef0-210">INPUTS</span></span>

### <span data-ttu-id="21ef0-211">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="21ef0-211">System.String</span></span>

### <span data-ttu-id="21ef0-212">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="21ef0-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="21ef0-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="21ef0-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="21ef0-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="21ef0-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="21ef0-215">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="21ef0-215">System.String[]</span></span>

### <span data-ttu-id="21ef0-216">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="21ef0-216">System.Int32</span></span>

## <span data-ttu-id="21ef0-217">출력</span><span class="sxs-lookup"><span data-stu-id="21ef0-217">OUTPUTS</span></span>

### <span data-ttu-id="21ef0-218">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="21ef0-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="21ef0-219">상속자</span><span class="sxs-lookup"><span data-stu-id="21ef0-219">NOTES</span></span>

## <span data-ttu-id="21ef0-220">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21ef0-220">RELATED LINKS</span></span>
