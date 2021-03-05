---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 13db3232c7d3f2245c6a99ac9a5d38054d885a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991256"
---
# <span data-ttu-id="be414-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="be414-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="be414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be414-102">SYNOPSIS</span></span>
<span data-ttu-id="be414-103">토픽, Azure 리소스, Azure 구독 또는 리소스 그룹에 새 Azure Event Grid 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="be414-104">구문</span><span class="sxs-lookup"><span data-stu-id="be414-104">SYNTAX</span></span>

### <span data-ttu-id="be414-105">ResourceGroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="be414-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be414-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be414-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be414-113">설명</span><span class="sxs-lookup"><span data-stu-id="be414-113">DESCRIPTION</span></span>
<span data-ttu-id="be414-114">Azure Event Grid 토픽, 지원되는 Azure 리소스, Azure 구독 또는 리소스 그룹에 대한 새 이벤트 구독을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="be414-115">현재 선택한 Azure 구독에 대한 이벤트 구독을 만들하려면 이벤트 구독 이름 및 대상 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="be414-116">리소스 그룹에 대한 이벤트 구독을 만들하려면 이벤트 구독 이름 및 대상 엔드포인트 외에도 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="be414-117">Azure Event Grid 토픽에 대한 이벤트 구독을 만들 경우 토픽 이름도 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="be414-118">지원되는 Azure 리소스에 대한 이벤트 구독을 만들하려면 리소스의 전체 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="be414-119">지원되는 형식 목록을 보기 위해 Get-AzEventGridTopicType cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="be414-120">예제</span><span class="sxs-lookup"><span data-stu-id="be414-120">EXAMPLES</span></span>

### <span data-ttu-id="be414-121">예제 1</span><span class="sxs-lookup"><span data-stu-id="be414-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be414-122">웹후크 대상 엔드포인트를 사용하여 리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 Azure Event Grid 토픽 토픽1에 새 이벤트 구독 EventSubscription1을 \` `https://requestb.in/19qlscd1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="be414-123">이 이벤트 구독은 기본 필터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="be414-124">예제 2</span><span class="sxs-lookup"><span data-stu-id="be414-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be414-125">웹후크 대상 엔드포인트를 통해 리소스 그룹에 \` \` \` MyResourceGroupName에 새 이벤트 구독 EventSubscription1을 \` `https://requestb.in/19qlscd1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="be414-126">이 이벤트 구독은 기본 필터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="be414-127">예제 3</span><span class="sxs-lookup"><span data-stu-id="be414-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be414-128">웹후크 대상 엔드포인트를 사용하여 현재 선택한 Azure 구독에 새 이벤트 구독 \` EventSubscription1을 \` `https://requestb.in/19qlscd1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="be414-129">이 이벤트 구독은 기본 필터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="be414-130">예제 4</span><span class="sxs-lookup"><span data-stu-id="be414-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="be414-131">웹후크 대상 엔드포인트를 사용하여 현재 선택한 Azure 구독에 새 이벤트 구독 \` EventSubscription1을 \` `https://requestb.in/19qlscd1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="be414-132">이 이벤트 구독은 이벤트 유형 및 제목에 대한 추가 필터를 지정하고 해당 필터와 일치하는 이벤트만 대상 엔드포인트로 배달됩니다.</span><span class="sxs-lookup"><span data-stu-id="be414-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="be414-133">예제 5</span><span class="sxs-lookup"><span data-stu-id="be414-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="be414-134">지정된 이벤트 허브를 이벤트의 대상으로 사용하여 현재 선택한 Azure 구독에 새 이벤트 구독 \` EventSubscription1을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="be414-135">이 이벤트 구독은 기본 필터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="be414-136">예제 6</span><span class="sxs-lookup"><span data-stu-id="be414-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="be414-137">지정된 웹후크 대상 엔드포인트가 있는 \` EventHub 네임스페이스에 EventSubscription1 새 이벤트 \` 구독을 `https://requestb.in/19qlscd1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be414-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="be414-138">이 이벤트 구독은 기본 필터를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="be414-139">매개 변수</span><span class="sxs-lookup"><span data-stu-id="be414-139">PARAMETERS</span></span>

### <span data-ttu-id="be414-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="be414-140">-AdvancedFilter</span></span>
<span data-ttu-id="be414-141">특성 기반 필터링에 사용되는 여러 해시테이블 값의 배열을 지정하는 고급 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="be414-142">각 해시테이블 값에는 작업, 키 및 값 또는 값과 같은 키 값 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="be414-143">연산자는 NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith 또는 StringContains일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="be414-144">키는 고급 필터링 정책이 적용되는 페이로드 속성을 나타 내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="be414-145">마지막으로 값 또는 값은 일치할 값 또는 값 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be414-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="be414-146">해당 형식의 단일 값 또는 값 배열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="be414-147">고급 필터 매개 변수의 예로 $AdvancedFilters=@($AdvFilter 1, $AdvFilter 2) 여기서 $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} 및 $AdvFilter 2=@{operator="StringBringsWith"; key="subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="be414-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="be414-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="be414-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="be414-149">AAD(Azure Active Directory) 애플리케이션 ID 또는 Uri를 사용하여 전달 요청에 전달자 토큰으로 포함될 액세스 토큰을 얻습니다. 대상 웹후크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be414-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="be414-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="be414-151">배달 요청에 전달자 토큰으로 포함될 액세스 토큰을 얻을 수 있는 AAD(Azure Active Directory) 테넌트 ID입니다. 대상 웹후크에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be414-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="be414-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="be414-153">검색되지 않은 이벤트를 저장하는 데 사용되는 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="be414-154">Storage Blob 컨테이너의 Azure 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="be414-155">예: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="be414-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="be414-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be414-156">-DefaultProfile</span></span>
<span data-ttu-id="be414-157">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="be414-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be414-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="be414-158">-DeliverySchema</span></span>
<span data-ttu-id="be414-159">대상에 이벤트를 배달할 때 사용할 스마.</span><span class="sxs-lookup"><span data-stu-id="be414-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="be414-160">가능한 값은 eventgridschema, CustomInputSchema 또는 cloudeventv01schema입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="be414-161">기본값은 CustomInputSchema입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

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
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be414-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="be414-162">-DomainInputObject</span></span>
<span data-ttu-id="be414-163">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="be414-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="be414-164">-DomainName</span></span>
<span data-ttu-id="be414-165">이벤트 구독을 만들어야 하는 Event Grid 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="be414-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="be414-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="be414-167">EventGrid 도메인 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="be414-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="be414-168">-DomainTopicName</span></span>
<span data-ttu-id="be414-169">이벤트 구독을 만들어야 하는 도메인 토픽의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="be414-170">-엔드포인트</span><span class="sxs-lookup"><span data-stu-id="be414-170">-Endpoint</span></span>
<span data-ttu-id="be414-171">이벤트 구독 대상 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="be414-172">웹후크 URL 또는 EventHub, 저장소 큐, 하이브리드 연결 또는 servicebusqueue의 Azure 리소스 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="be414-173">예를 들어 하이브리드 연결에 대한 리소스 ID는 /subscriptions/[Azure 구독 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]을 폼으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="be414-174">Event Grid cmdlet을 실행하기 전에 대상 엔드포인트를 만들어 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="be414-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="be414-175">-EndpointType</span></span>
<span data-ttu-id="be414-176">엔드포인트 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-176">Endpoint Type.</span></span>
<span data-ttu-id="be414-177">웹후크, eventhub, storagequeue, hybridconnection 또는 servicebusqueue일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="be414-178">기본값은 웹후크입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

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
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be414-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="be414-179">-EventSubscriptionName</span></span>
<span data-ttu-id="be414-180">이벤트 구독의 이름</span><span class="sxs-lookup"><span data-stu-id="be414-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="be414-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="be414-181">-EventTtl</span></span>
<span data-ttu-id="be414-182">이벤트 배달 시간(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="be414-183">이 값은 1에서 1440 사이일 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="be414-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="be414-184">-ExpirationDate</span></span>
<span data-ttu-id="be414-185">이벤트 구독이 사용 중지되는 이벤트 구독에 대한 만료 DateTime을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="be414-186">-includedEventType</span><span class="sxs-lookup"><span data-stu-id="be414-186">-IncludedEventType</span></span>
<span data-ttu-id="be414-187">포함할 이벤트 형식 목록을 지정하는 필터입니다. 지정하지 않으면 모든 이벤트 형식이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="be414-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be414-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be414-188">-InputObject</span></span>
<span data-ttu-id="be414-189">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="be414-190">-Label</span><span class="sxs-lookup"><span data-stu-id="be414-190">-Label</span></span>
<span data-ttu-id="be414-191">이벤트 구독에 대한 레이블</span><span class="sxs-lookup"><span data-stu-id="be414-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be414-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="be414-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="be414-193">이벤트를 배달하려는 최대 시도 수입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="be414-194">이 값은 1~30 사이의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="be414-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="be414-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="be414-196">일괄 처리의 최대 이벤트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="be414-197">이 값은 1에서 5000 사이일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="be414-198">이 매개 변수는 Endpint Type이 웹후크일 때만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="be414-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="be414-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="be414-200">기본 배치 크기는 킬로바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="be414-201">이 값은 1에서 1024 사이일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="be414-202">이 매개 변수는 Endpint Type이 웹후크일 때만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="be414-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be414-203">-ResourceGroupName</span></span>
<span data-ttu-id="be414-204">토픽의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="be414-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be414-205">-ResourceId</span></span>
<span data-ttu-id="be414-206">이벤트 구독을 만들어야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="be414-207">-subjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="be414-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="be414-208">지정된 제목과 일치하는 이벤트만 포함될 것을 지정하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="be414-209">지정하지 않으면 모든 제목의 사전이 포함된 이벤트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="be414-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="be414-210">-subjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="be414-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="be414-211">대소문자 구분 방식으로 제목 필드를 비교해야 한다고 지정하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="be414-212">지정하지 않으면 제목은 대소문자에 대해 무관하게 비교됩니다.</span><span class="sxs-lookup"><span data-stu-id="be414-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="be414-213">-subjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="be414-213">-SubjectEndsWith</span></span>
<span data-ttu-id="be414-214">지정된 제목 접미사와 일치하는 이벤트만 포함되는 것을 지정하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="be414-215">지정하지 않으면 모든 제목 접미사가 포함된 이벤트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="be414-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="be414-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="be414-216">-TopicName</span></span>
<span data-ttu-id="be414-217">이벤트 구독을 만들어야 하는 토픽의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be414-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="be414-218">-확인</span><span class="sxs-lookup"><span data-stu-id="be414-218">-Confirm</span></span>
<span data-ttu-id="be414-219">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="be414-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be414-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be414-220">-WhatIf</span></span>
<span data-ttu-id="be414-221">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="be414-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be414-222">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be414-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be414-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be414-223">CommonParameters</span></span>
<span data-ttu-id="be414-224">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be414-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be414-225">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be414-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be414-226">입력</span><span class="sxs-lookup"><span data-stu-id="be414-226">INPUTS</span></span>

### <span data-ttu-id="be414-227">System.String</span><span class="sxs-lookup"><span data-stu-id="be414-227">System.String</span></span>

### <span data-ttu-id="be414-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="be414-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="be414-229">Microsoft.Azure.Commands.EventGrid.Models.PSD오마인</span><span class="sxs-lookup"><span data-stu-id="be414-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="be414-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="be414-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="be414-231">System.String[]</span><span class="sxs-lookup"><span data-stu-id="be414-231">System.String[]</span></span>

### <span data-ttu-id="be414-232">System.Int32</span><span class="sxs-lookup"><span data-stu-id="be414-232">System.Int32</span></span>

## <span data-ttu-id="be414-233">출력</span><span class="sxs-lookup"><span data-stu-id="be414-233">OUTPUTS</span></span>

### <span data-ttu-id="be414-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="be414-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="be414-235">참고 사항</span><span class="sxs-lookup"><span data-stu-id="be414-235">NOTES</span></span>

## <span data-ttu-id="be414-236">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be414-236">RELATED LINKS</span></span>
