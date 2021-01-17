---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342146"
---
# <span data-ttu-id="6082b-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6082b-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="6082b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6082b-102">SYNOPSIS</span></span>
<span data-ttu-id="6082b-103">Event Grid 이벤트 구독의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="6082b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6082b-104">SYNTAX</span></span>

### <span data-ttu-id="6082b-105">ResourceGroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6082b-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6082b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6082b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6082b-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6082b-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6082b-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6082b-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6082b-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6082b-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6082b-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6082b-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6082b-111">설명</span><span class="sxs-lookup"><span data-stu-id="6082b-111">DESCRIPTION</span></span>
<span data-ttu-id="6082b-112">Event Grid 이벤트 구독의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="6082b-113">기존 이벤트 구독의 필터, 대상 또는 레이블을 업데이트하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="6082b-114">예제</span><span class="sxs-lookup"><span data-stu-id="6082b-114">EXAMPLES</span></span>

### <span data-ttu-id="6082b-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="6082b-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="6082b-116">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 topic1에 대한 이벤트 구독 ES1의 엔드포인트를 \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="6082b-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="6082b-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="6082b-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="6082b-118">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 topic1에 대한 이벤트 구독 ES1의 엔드포인트를 \`\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="6082b-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="6082b-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="6082b-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="6082b-120">EventHub 네임스페이스 \` ContosoNamespace에 대한 이벤트 구독 ES1의 속성을 새 엔드포인트 '로, 새 \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith 필터를 \` jpg로 업데이트합니다.\`</span><span class="sxs-lookup"><span data-stu-id="6082b-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="6082b-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="6082b-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="6082b-122">리소스 그룹 \` \` \` MyResourceGroupName에 대한 이벤트 구독 ES1의 속성을 새 레이블로 \` $labels.</span><span class="sxs-lookup"><span data-stu-id="6082b-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="6082b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6082b-123">PARAMETERS</span></span>

### <span data-ttu-id="6082b-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="6082b-124">-AdvancedFilter</span></span>
<span data-ttu-id="6082b-125">특성 기반 필터링에 사용되는 여러 해시블 값의 배열을 지정하는 고급 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="6082b-126">각 해시블 값에는 작업, 키 및 값 또는 값과 같은 키-값 정보가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="6082b-127">연산자는 NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith 또는 StringContains 값 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="6082b-128">키는 고급 필터링 정책이 적용되는 페이로드 속성을 나타내며,</span><span class="sxs-lookup"><span data-stu-id="6082b-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="6082b-129">마지막으로 값 또는 값은 일치할 값 또는 값 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="6082b-130">해당 형식의 단일 값 또는 값 배열일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="6082b-131">고급 필터 매개 변수의 예로 $AdvancedFilters=@($AdvFilter 1, $AdvFilter 2) where $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} 및 $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="6082b-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="6082b-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="6082b-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="6082b-133">배달 요청에 전달자 토큰으로 포함될 액세스 토큰을 얻을 수 있는 AAD(Azure Active Directory) 애플리케이션 ID 또는 URI입니다. 웹후크를 대상으로만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="6082b-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="6082b-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="6082b-135">배달 요청에 전달자 토큰으로 포함될 액세스 토큰을 얻을 수 있는 AAD(Azure Active Directory) 테넌트 ID입니다. 웹후크를 대상으로만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="6082b-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="6082b-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="6082b-137">검색되지 않은 이벤트를 저장하는 데 사용되는 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="6082b-138">Storage Blob 컨테이너의 Azure 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="6082b-139">예: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="6082b-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="6082b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6082b-140">-DefaultProfile</span></span>
<span data-ttu-id="6082b-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6082b-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="6082b-142">-DomainName</span></span>
<span data-ttu-id="6082b-143">이벤트 구독을 만들어야 하는 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6082b-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="6082b-144">-DomainTopicName</span></span>
<span data-ttu-id="6082b-145">이벤트 구독을 만들어야 하는 도메인 토픽의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6082b-146">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="6082b-146">-Endpoint</span></span>
<span data-ttu-id="6082b-147">이벤트 구독 대상 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="6082b-148">이는 웹후크 URL 또는 EventHub, 저장소 큐, hybridconnection 또는 servicebusqueue의 Azure 리소스 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="6082b-149">예를 들어 하이브리드 연결에 대한 리소스 ID는 /subscriptions/[Azure 구독 ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName]을 하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="6082b-150">Event Grid cmdlet을 실행하기 전에 대상 엔드포인트를 만들어 사용할 수 있을 것으로 예상됩니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="6082b-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6082b-151">-EndpointType</span></span>
<span data-ttu-id="6082b-152">엔드포인트 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-152">Endpoint Type.</span></span>
<span data-ttu-id="6082b-153">웹후크, eventhub, storagequeue, hybridconnection 또는 servicebusqueue일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="6082b-154">기본값은 웹후크입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="6082b-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6082b-155">-EventSubscriptionName</span></span>
<span data-ttu-id="6082b-156">이벤트 구독의 이름</span><span class="sxs-lookup"><span data-stu-id="6082b-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="6082b-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="6082b-157">-EventTtl</span></span>
<span data-ttu-id="6082b-158">이벤트 배달에 대한 시간(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="6082b-159">이 값은 1에서 1440 사이로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="6082b-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="6082b-160">-ExpirationDate</span></span>
<span data-ttu-id="6082b-161">이벤트 구독이 사용 중지되는 이벤트 구독에 대한 만료 DateTime을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="6082b-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="6082b-162">-IncludedEventType</span></span>
<span data-ttu-id="6082b-163">포함할 이벤트 유형 목록을 지정하는 필터입니다. 지정하지 않으면 모든 이벤트 유형이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="6082b-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6082b-164">-InputObject</span></span>
<span data-ttu-id="6082b-165">EventGridSubscription 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="6082b-166">-Label</span><span class="sxs-lookup"><span data-stu-id="6082b-166">-Label</span></span>
<span data-ttu-id="6082b-167">이벤트 구독에 대한 레이블</span><span class="sxs-lookup"><span data-stu-id="6082b-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="6082b-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="6082b-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="6082b-169">이벤트를 배달하려는 최대 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="6082b-170">이 값은 1에서 30 사이로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="6082b-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="6082b-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="6082b-172">일괄 처리의 최대 이벤트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="6082b-173">이 값은 1에서 5000 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="6082b-174">이 매개 변수는 Endpint 형식이 웹후크일 때만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="6082b-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="6082b-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="6082b-176">기본 배치 크기(킬로바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="6082b-177">이 값은 1에서 1024 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="6082b-178">이 매개 변수는 Endpint 형식이 웹후크일 때만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="6082b-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6082b-179">-ResourceGroupName</span></span>
<span data-ttu-id="6082b-180">토픽의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="6082b-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6082b-181">-ResourceId</span></span>
<span data-ttu-id="6082b-182">이벤트 구독이 만들어진 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="6082b-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="6082b-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="6082b-184">지정된 주체와 일치하는 이벤트만 포함 하게 지정하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="6082b-185">지정하지 않으면 모든 주체 사전이 포함된 이벤트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="6082b-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="6082b-186">-SubjectEndsWith</span></span>
<span data-ttu-id="6082b-187">지정된 주체 접미사와 일치하는 이벤트만 포함 하게 지정하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="6082b-188">지정하지 않으면 모든 주체 접미사가 있는 이벤트가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="6082b-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6082b-189">-TopicName</span></span>
<span data-ttu-id="6082b-190">이벤트 구독을 만들어야 하는 토픽의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6082b-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6082b-191">-Confirm</span></span>
<span data-ttu-id="6082b-192">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6082b-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6082b-193">-WhatIf</span></span>
<span data-ttu-id="6082b-194">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6082b-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6082b-195">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6082b-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6082b-196">CommonParameters</span></span>
<span data-ttu-id="6082b-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6082b-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6082b-198">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6082b-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6082b-199">입력</span><span class="sxs-lookup"><span data-stu-id="6082b-199">INPUTS</span></span>

### <span data-ttu-id="6082b-200">System.String</span><span class="sxs-lookup"><span data-stu-id="6082b-200">System.String</span></span>

### <span data-ttu-id="6082b-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="6082b-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="6082b-202">출력</span><span class="sxs-lookup"><span data-stu-id="6082b-202">OUTPUTS</span></span>

### <span data-ttu-id="6082b-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="6082b-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="6082b-204">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6082b-204">NOTES</span></span>

## <span data-ttu-id="6082b-205">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6082b-205">RELATED LINKS</span></span>
