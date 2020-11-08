---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214977"
---
# <span data-ttu-id="14425-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="14425-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="14425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14425-102">SYNOPSIS</span></span>
<span data-ttu-id="14425-103">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="14425-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14425-104">SYNTAX</span></span>

### <span data-ttu-id="14425-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="14425-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14425-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14425-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14425-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14425-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14425-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14425-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14425-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14425-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14425-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14425-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14425-111">설명은</span><span class="sxs-lookup"><span data-stu-id="14425-111">DESCRIPTION</span></span>
<span data-ttu-id="14425-112">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="14425-113">이를 사용 하 여 기존 이벤트 구독의 필터, 대상 또는 레이블을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="14425-114">예제의</span><span class="sxs-lookup"><span data-stu-id="14425-114">EXAMPLES</span></span>

### <span data-ttu-id="14425-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="14425-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="14425-116">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="14425-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="14425-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="14425-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="14425-118">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="14425-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="14425-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="14425-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="14425-120">\` \` 새 끝점 as \` https://requestb.in/1kxxoui1\ ' 및 새 부분 endswith 필터를 jpg로 사용 하 여 EventHub 네임 스페이스 ContosoNamespace에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .\`</span><span class="sxs-lookup"><span data-stu-id="14425-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="14425-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="14425-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="14425-122">\` \` \` $Labels 새 레이블이 있는 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="14425-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="14425-123">변수</span><span class="sxs-lookup"><span data-stu-id="14425-123">PARAMETERS</span></span>

### <span data-ttu-id="14425-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="14425-124">-AdvancedFilter</span></span>
<span data-ttu-id="14425-125">특성 기반 필터링에 사용 되는 여러 해시 테이블 값의 배열을 지정 하는 고급 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="14425-126">각 해시 테이블 값에는 작업, 키, 값 또는 값의 키 값 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="14425-127">Operator는 번호 In, 숫자 Notin, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, Stringin 또는 Stringin 값 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="14425-128">Key는 고급 필터링 정책이 적용 되는 페이로드 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14425-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="14425-129">마지막으로 값 또는 값은 일치 시킬 값 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14425-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="14425-130">해당 형식 또는 값의 배열에 대 한 단일 값이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="14425-131">고급 필터 매개 변수의 예: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) $AdvFilter 1 = @ {연산자 = "숫자 In", key = "Data. Key1"; 값 = @ (1, 2)} 및 $AdvFilter 2 = @ {operator = "StringBeginsWith"; key = "Subject"; 값 = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="14425-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="14425-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="14425-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="14425-133">배달 요청에 전달자 토큰으로 포함 될 액세스 토큰을 가져오기 위한 AAD (Azure Active Directory) 응용 프로그램 Id 또는 Uri입니다. Webhook에는 대상으로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14425-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="14425-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="14425-135">배달 요청에 전달자 토큰으로 포함 될 액세스 토큰을 가져오기 위한 AAD (Azure Active Directory) 테 넌 트 Id입니다. Webhook에는 대상으로 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14425-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="14425-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="14425-137">배달 되지 않은 이벤트를 저장 하는 데 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="14425-138">저장소 blob 컨테이너의 Azure 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="14425-139">예:/subscriptions/[SubscriptionId]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="14425-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="14425-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14425-140">-DefaultProfile</span></span>
<span data-ttu-id="14425-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14425-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="14425-142">-DomainName</span></span>
<span data-ttu-id="14425-143">이벤트 구독을 만들어야 하는 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="14425-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="14425-144">-DomainTopicName</span></span>
<span data-ttu-id="14425-145">이벤트 구독을 만들어야 하는 도메인 항목의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="14425-146">-끝점</span><span class="sxs-lookup"><span data-stu-id="14425-146">-Endpoint</span></span>
<span data-ttu-id="14425-147">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="14425-148">이는 webhook URL 또는 EventHub, storage queue, hybridconnection 또는 servicebusqueue의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="14425-149">예를 들어 하이브리드 연결의 리소스 ID에는/subscriptions/[Azure 구독 ID]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName] 형식이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="14425-150">이벤트 그리드 cmdlet을 실행 하기 전에 대상 끝점을 만들어 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="14425-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="14425-151">-EndpointType</span></span>
<span data-ttu-id="14425-152">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-152">Endpoint Type.</span></span>
<span data-ttu-id="14425-153">이는 webhook, eventhub, storagequeue, hybridconnection 또는 servicebusqueue 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="14425-154">기본값은 webhook입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14425-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="14425-155">-EventSubscriptionName</span></span>
<span data-ttu-id="14425-156">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="14425-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="14425-157">-EventTtl</span></span>
<span data-ttu-id="14425-158">이벤트 배달을 위한 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="14425-159">이 값은 1에서 1440 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="14425-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="14425-160">-ExpirationDate</span></span>
<span data-ttu-id="14425-161">이벤트 구독이 중지 될 때 이벤트 구독에 대 한 만료 날짜/시간을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="14425-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="14425-162">-IncludedEventType</span></span>
<span data-ttu-id="14425-163">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14425-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="14425-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14425-164">-InputObject</span></span>
<span data-ttu-id="14425-165">EventGridSubscription 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="14425-166">-레이블</span><span class="sxs-lookup"><span data-stu-id="14425-166">-Label</span></span>
<span data-ttu-id="14425-167">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="14425-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="14425-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="14425-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="14425-169">이벤트 배달을 위한 최대 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="14425-170">이 값은 1에서 30 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="14425-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="14425-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="14425-172">일괄 처리의 최대 이벤트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="14425-173">이 값은 1에서 5000 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="14425-174">이 매개 변수는 Endpint 형식이 webhook 인 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="14425-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="14425-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="14425-176">기본 설정 일괄 처리 크기 (kb)입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="14425-177">이 값은 1에서 1024 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="14425-178">이 매개 변수는 Endpint 형식이 webhook 인 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="14425-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14425-179">-ResourceGroupName</span></span>
<span data-ttu-id="14425-180">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="14425-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14425-181">-ResourceId</span></span>
<span data-ttu-id="14425-182">이벤트 구독이 만들어진 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="14425-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="14425-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="14425-184">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="14425-185">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14425-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="14425-186">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="14425-186">-SubjectEndsWith</span></span>
<span data-ttu-id="14425-187">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="14425-188">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14425-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="14425-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="14425-189">-TopicName</span></span>
<span data-ttu-id="14425-190">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14425-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="14425-191">-확인</span><span class="sxs-lookup"><span data-stu-id="14425-191">-Confirm</span></span>
<span data-ttu-id="14425-192">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14425-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14425-193">-WhatIf</span></span>
<span data-ttu-id="14425-194">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14425-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14425-195">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14425-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14425-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14425-196">CommonParameters</span></span>
<span data-ttu-id="14425-197">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14425-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14425-198">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14425-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14425-199">입력</span><span class="sxs-lookup"><span data-stu-id="14425-199">INPUTS</span></span>

### <span data-ttu-id="14425-200">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14425-200">System.String</span></span>

### <span data-ttu-id="14425-201">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="14425-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="14425-202">출력</span><span class="sxs-lookup"><span data-stu-id="14425-202">OUTPUTS</span></span>

### <span data-ttu-id="14425-203">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="14425-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="14425-204">상속자</span><span class="sxs-lookup"><span data-stu-id="14425-204">NOTES</span></span>

## <span data-ttu-id="14425-205">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14425-205">RELATED LINKS</span></span>
