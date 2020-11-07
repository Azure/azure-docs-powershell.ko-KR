---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: eaf9a89a8c610d8666a356e563681accfced4a7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696505"
---
# <span data-ttu-id="a338a-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a338a-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="a338a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a338a-102">SYNOPSIS</span></span>
<span data-ttu-id="a338a-103">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="a338a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a338a-104">SYNTAX</span></span>

### <span data-ttu-id="a338a-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a338a-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a338a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a338a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a338a-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a338a-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a338a-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a338a-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a338a-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a338a-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a338a-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a338a-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a338a-111">설명은</span><span class="sxs-lookup"><span data-stu-id="a338a-111">DESCRIPTION</span></span>
<span data-ttu-id="a338a-112">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="a338a-113">이를 사용 하 여 기존 이벤트 구독의 필터, 대상 또는 레이블을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="a338a-114">예제의</span><span class="sxs-lookup"><span data-stu-id="a338a-114">EXAMPLES</span></span>

### <span data-ttu-id="a338a-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="a338a-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="a338a-116">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="a338a-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="a338a-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="a338a-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="a338a-118">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="a338a-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="a338a-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="a338a-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="a338a-120">\` \` 새 끝점 as \` https://requestb.in/1kxxoui1\ ' 및 새 부분 endswith 필터를 jpg로 사용 하 여 EventHub 네임 스페이스 ContosoNamespace에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .\`</span><span class="sxs-lookup"><span data-stu-id="a338a-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="a338a-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="a338a-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="a338a-122">\` \` \` $Labels 새 레이블이 있는 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="a338a-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="a338a-123">변수</span><span class="sxs-lookup"><span data-stu-id="a338a-123">PARAMETERS</span></span>

### <span data-ttu-id="a338a-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="a338a-124">-AdvancedFilter</span></span>
<span data-ttu-id="a338a-125">특성 기반 필터링에 사용 되는 여러 해시 테이블 값의 배열을 지정 하는 고급 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="a338a-126">각 해시 테이블 값에는 작업, 키, 값 또는 값의 키 값 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="a338a-127">Operator는 번호 In, 숫자 Notin, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, Stringin 또는 Stringin 값 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="a338a-128">Key는 고급 필터링 정책이 적용 되는 페이로드 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="a338a-129">마지막으로 값 또는 값은 일치 시킬 값 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="a338a-130">해당 형식 또는 값의 배열에 대 한 단일 값이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="a338a-131">고급 필터 매개 변수의 예: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) $AdvFilter 1 = @ {연산자 = "숫자 In", key = "Data. Key1"; 값 = @ (1, 2)} 및 $AdvFilter 2 = @ {operator = "StringBringsWith"; key = "Subject"; 값 = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="a338a-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="a338a-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="a338a-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="a338a-133">배달 되지 않은 이벤트를 저장 하는 데 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="a338a-134">저장소 blob 컨테이너의 Azure 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="a338a-135">예:/subscriptions/[SubscriptionId]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="a338a-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a338a-136">-DefaultProfile</span></span>
<span data-ttu-id="a338a-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a338a-138">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a338a-138">-DomainName</span></span>
<span data-ttu-id="a338a-139">이벤트 구독을 만들어야 하는 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a338a-140">-DomainTopicName</span></span>
<span data-ttu-id="a338a-141">이벤트 구독을 만들어야 하는 도메인 항목의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-142">-끝점</span><span class="sxs-lookup"><span data-stu-id="a338a-142">-Endpoint</span></span>
<span data-ttu-id="a338a-143">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="a338a-144">이는 webhook URL 또는 EventHub, storage queue, hybridconnection 또는 servicebusqueue의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="a338a-145">예를 들어 하이브리드 연결의 리소스 ID에는/subscriptions/[Azure 구독 ID]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName] 형식이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="a338a-146">이벤트 그리드 cmdlet을 실행 하기 전에 대상 끝점을 만들어 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a338a-147">-EndpointType</span></span>
<span data-ttu-id="a338a-148">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-148">Endpoint Type.</span></span>
<span data-ttu-id="a338a-149">이는 webhook, eventhub, storagequeue, hybridconnection 또는 servicebusqueue 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="a338a-150">기본값은 webhook입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a338a-151">-EventSubscriptionName</span></span>
<span data-ttu-id="a338a-152">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="a338a-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="a338a-153">-EventTtl</span></span>
<span data-ttu-id="a338a-154">이벤트 배달을 위한 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="a338a-155">이 값은 1에서 1440 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-156">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="a338a-156">-ExpirationDate</span></span>
<span data-ttu-id="a338a-157">이벤트 구독이 중지 될 때 이벤트 구독에 대 한 만료 날짜/시간을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="a338a-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="a338a-158">-IncludedEventType</span></span>
<span data-ttu-id="a338a-159">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a338a-160">-InputObject</span></span>
<span data-ttu-id="a338a-161">EventGridSubscription 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-161">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-162">-레이블</span><span class="sxs-lookup"><span data-stu-id="a338a-162">-Label</span></span>
<span data-ttu-id="a338a-163">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="a338a-163">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="a338a-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="a338a-165">이벤트 배달을 위한 최대 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="a338a-166">이 값은 1에서 30 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-166">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a338a-167">-ResourceGroupName</span></span>
<span data-ttu-id="a338a-168">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-168">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a338a-169">-ResourceId</span></span>
<span data-ttu-id="a338a-170">이벤트 구독이 만들어진 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="a338a-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="a338a-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="a338a-172">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="a338a-173">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-173">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-174">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="a338a-174">-SubjectEndsWith</span></span>
<span data-ttu-id="a338a-175">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="a338a-176">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-176">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a338a-177">-TopicName</span></span>
<span data-ttu-id="a338a-178">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-178">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a338a-179">-확인</span><span class="sxs-lookup"><span data-stu-id="a338a-179">-Confirm</span></span>
<span data-ttu-id="a338a-180">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a338a-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a338a-181">-WhatIf</span></span>
<span data-ttu-id="a338a-182">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a338a-183">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a338a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a338a-184">CommonParameters</span></span>
<span data-ttu-id="a338a-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a338a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a338a-186">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a338a-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a338a-187">입력</span><span class="sxs-lookup"><span data-stu-id="a338a-187">INPUTS</span></span>

### <span data-ttu-id="a338a-188">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a338a-188">System.String</span></span>

### <span data-ttu-id="a338a-189">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="a338a-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a338a-190">출력</span><span class="sxs-lookup"><span data-stu-id="a338a-190">OUTPUTS</span></span>

### <span data-ttu-id="a338a-191">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="a338a-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a338a-192">상속자</span><span class="sxs-lookup"><span data-stu-id="a338a-192">NOTES</span></span>

## <span data-ttu-id="a338a-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a338a-193">RELATED LINKS</span></span>
