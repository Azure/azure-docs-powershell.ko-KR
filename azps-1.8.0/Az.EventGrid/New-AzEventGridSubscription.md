---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395189"
---
# <span data-ttu-id="6740d-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6740d-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="6740d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6740d-102">SYNOPSIS</span></span>
<span data-ttu-id="6740d-103">항목, Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 Azure 이벤트 그리드 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="6740d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6740d-104">SYNTAX</span></span>

### <span data-ttu-id="6740d-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6740d-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6740d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6740d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6740d-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6740d-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6740d-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6740d-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6740d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6740d-109">DESCRIPTION</span></span>
<span data-ttu-id="6740d-110">Azure 이벤트 그리드 항목, 지원 되는 Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="6740d-111">현재 선택 된 Azure 구독에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="6740d-112">리소스 그룹에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점 외에도 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="6740d-113">Azure 이벤트 그리드 항목에 대 한 이벤트 구독을 만들려면 항목 이름도 함께 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="6740d-114">지원 되는 Azure 리소스에 대 한 이벤트 구독을 만들려면 리소스의 전체 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="6740d-115">지원 되는 형식 목록을 보려면 Get-AzEventGridTopicType cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="6740d-116">예제의</span><span class="sxs-lookup"><span data-stu-id="6740d-116">EXAMPLES</span></span>

### <span data-ttu-id="6740d-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="6740d-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6740d-118">\` \` \` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName에서 Azure 이벤트 그리드 항목 Topic1에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="6740d-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6740d-119">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6740d-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="6740d-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6740d-121">\` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="6740d-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6740d-122">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6740d-123">예제 3</span><span class="sxs-lookup"><span data-stu-id="6740d-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6740d-124">\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="6740d-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6740d-125">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6740d-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="6740d-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="6740d-127">\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="6740d-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6740d-128">이 이벤트 구독은 이벤트 유형 및 주체의 추가 필터를 지정 하 고 해당 필터와 일치 하는 이벤트만 대상 끝점에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="6740d-129">예제 5</span><span class="sxs-lookup"><span data-stu-id="6740d-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="6740d-130">\` \` 지정 된 이벤트 허브가 있는 현재 선택한 Azure 구독에 대 한 EventSubscription1 이벤트의 대상으로 새 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="6740d-131">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="6740d-132">예제 6</span><span class="sxs-lookup"><span data-stu-id="6740d-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="6740d-133">\` \` 지정 된 webhook 대상 끝점을 사용 하 여 EventHub 네임 스페이스에 EventSubscription1 새 이벤트 구독을 만듭니다 `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="6740d-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="6740d-134">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="6740d-135">변수</span><span class="sxs-lookup"><span data-stu-id="6740d-135">PARAMETERS</span></span>

### <span data-ttu-id="6740d-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="6740d-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="6740d-137">배달 되지 않은 이벤트를 저장 하는 데 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="6740d-138">저장소 blob 컨테이너의 Azure 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="6740d-139">예:/subscriptions/[SubscriptionId]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="6740d-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6740d-140">-DefaultProfile</span></span>
<span data-ttu-id="6740d-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6740d-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6740d-142">-끝점</span><span class="sxs-lookup"><span data-stu-id="6740d-142">-Endpoint</span></span>
<span data-ttu-id="6740d-143">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="6740d-144">이는 webhook URL 또는 EventHub, storage queue 또는 hybridconnection의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="6740d-145">예를 들어 하이브리드 연결의 리소스 ID에는/subscriptions/[Azure 구독 ID]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName] 형식이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="6740d-146">이벤트 그리드 cmdlet을 실행 하기 전에 대상 끝점을 만들어 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6740d-147">-EndpointType</span></span>
<span data-ttu-id="6740d-148">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-148">Endpoint Type.</span></span>
<span data-ttu-id="6740d-149">이는 webhook, eventhub, storagequeue 또는 hybridconnection 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="6740d-150">기본값은 webhook입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6740d-151">-EventSubscriptionName</span></span>
<span data-ttu-id="6740d-152">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-152">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="6740d-153">-EventTtl</span></span>
<span data-ttu-id="6740d-154">이벤트 배달을 위한 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="6740d-155">이 값은 1에서 1440 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="6740d-156">-IncludedEventType</span></span>
<span data-ttu-id="6740d-157">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6740d-158">-InputObject</span></span>
<span data-ttu-id="6740d-159">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="6740d-159">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6740d-160">-레이블</span><span class="sxs-lookup"><span data-stu-id="6740d-160">-Label</span></span>
<span data-ttu-id="6740d-161">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="6740d-161">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="6740d-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="6740d-163">이벤트 배달을 위한 최대 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="6740d-164">이 값은 1에서 30 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6740d-165">-ResourceGroupName</span></span>
<span data-ttu-id="6740d-166">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-166">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6740d-167">-ResourceId</span></span>
<span data-ttu-id="6740d-168">이벤트 구독을 만들어야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6740d-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="6740d-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="6740d-170">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="6740d-171">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-171">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-172">-이란 Casesensitive</span><span class="sxs-lookup"><span data-stu-id="6740d-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="6740d-173">주제 필드가 대/소문자를 구분 하 여 비교 하도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="6740d-174">지정 하지 않으면 제목은 대/소문자를 구분 하지 않고 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="6740d-175">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="6740d-175">-SubjectEndsWith</span></span>
<span data-ttu-id="6740d-176">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="6740d-177">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-177">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6740d-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6740d-178">-TopicName</span></span>
<span data-ttu-id="6740d-179">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-179">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="6740d-180">-확인</span><span class="sxs-lookup"><span data-stu-id="6740d-180">-Confirm</span></span>
<span data-ttu-id="6740d-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6740d-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6740d-182">-WhatIf</span></span>
<span data-ttu-id="6740d-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6740d-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6740d-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6740d-185">CommonParameters</span></span>
<span data-ttu-id="6740d-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6740d-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6740d-187">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6740d-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6740d-188">입력</span><span class="sxs-lookup"><span data-stu-id="6740d-188">INPUTS</span></span>

### <span data-ttu-id="6740d-189">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6740d-189">System.String</span></span>

### <span data-ttu-id="6740d-190">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="6740d-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="6740d-191">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="6740d-191">System.String[]</span></span>

## <span data-ttu-id="6740d-192">출력</span><span class="sxs-lookup"><span data-stu-id="6740d-192">OUTPUTS</span></span>

### <span data-ttu-id="6740d-193">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="6740d-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="6740d-194">상속자</span><span class="sxs-lookup"><span data-stu-id="6740d-194">NOTES</span></span>

## <span data-ttu-id="6740d-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6740d-195">RELATED LINKS</span></span>
