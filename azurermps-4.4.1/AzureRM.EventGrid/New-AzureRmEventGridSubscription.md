---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537295"
---
# <span data-ttu-id="70616-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="70616-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="70616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70616-102">SYNOPSIS</span></span>
<span data-ttu-id="70616-103">항목, Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 Azure 이벤트 그리드 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70616-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70616-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70616-104">SYNTAX</span></span>

### <span data-ttu-id="70616-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="70616-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70616-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="70616-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70616-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70616-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70616-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="70616-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70616-109">설명은</span><span class="sxs-lookup"><span data-stu-id="70616-109">DESCRIPTION</span></span>
<span data-ttu-id="70616-110">Azure 이벤트 그리드 항목, 지원 되는 Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70616-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="70616-111">현재 선택 된 Azure 구독에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="70616-112">리소스 그룹에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점 외에도 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="70616-113">Azure 이벤트 그리드 항목에 대 한 이벤트 구독을 만들려면 항목 이름도 함께 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="70616-114">지원 되는 Azure 리소스에 대 한 이벤트 구독을 만들려면 리소스의 전체 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="70616-115">지원 되는 형식 목록을 보려면 Get-AzureRmEventGridTopicType cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="70616-116">예제의</span><span class="sxs-lookup"><span data-stu-id="70616-116">EXAMPLES</span></span>

### <span data-ttu-id="70616-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="70616-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70616-118">\` \` \` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName에서 Azure 이벤트 그리드 항목 Topic1에 EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="70616-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="70616-119">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="70616-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="70616-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70616-121">\` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="70616-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="70616-122">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="70616-123">예제 3</span><span class="sxs-lookup"><span data-stu-id="70616-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70616-124">\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="70616-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="70616-125">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="70616-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="70616-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="70616-127">\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="70616-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="70616-128">이 이벤트 구독은 이벤트 유형 및 주체의 추가 필터를 지정 하 고 해당 필터와 일치 하는 이벤트만 대상 끝점에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70616-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="70616-129">예제 5</span><span class="sxs-lookup"><span data-stu-id="70616-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="70616-130">\` \` 지정 된 이벤트 허브가 있는 현재 선택한 Azure 구독에 대 한 EventSubscription1 이벤트의 대상으로 새 이벤트 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="70616-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="70616-131">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="70616-132">예제 6</span><span class="sxs-lookup"><span data-stu-id="70616-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="70616-133">\` \` 지정 된 webhhok 대상 끝점을 사용 하 여 EventHub 네임 스페이스에 대 한 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="70616-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="70616-134">이 이벤트 구독은 기본 필터를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="70616-135">변수</span><span class="sxs-lookup"><span data-stu-id="70616-135">PARAMETERS</span></span>

### <span data-ttu-id="70616-136">-끝점</span><span class="sxs-lookup"><span data-stu-id="70616-136">-Endpoint</span></span>
<span data-ttu-id="70616-137">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-137">Event subscription destination endpoint.</span></span>
<span data-ttu-id="70616-138">이것은 webhook URL 또는 EventHub의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70616-138">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-139">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="70616-139">-EndpointType</span></span>
<span data-ttu-id="70616-140">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-140">Endpoint Type.</span></span>
<span data-ttu-id="70616-141">이는 webhook 또는 eventhub 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70616-141">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-142">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="70616-142">-EventSubscriptionName</span></span>
<span data-ttu-id="70616-143">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-143">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-144">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="70616-144">-IncludedEventType</span></span>
<span data-ttu-id="70616-145">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70616-145">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70616-146">-InputObject</span></span>
<span data-ttu-id="70616-147">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="70616-147">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-148">-레이블</span><span class="sxs-lookup"><span data-stu-id="70616-148">-Label</span></span>
<span data-ttu-id="70616-149">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="70616-149">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70616-150">-ResourceGroupName</span></span>
<span data-ttu-id="70616-151">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-151">The resource group of the topic.</span></span>

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

### <span data-ttu-id="70616-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70616-152">-ResourceId</span></span>
<span data-ttu-id="70616-153">이벤트 구독을 만들어야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-153">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="70616-154">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="70616-154">-SubjectBeginsWith</span></span>
<span data-ttu-id="70616-155">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-155">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="70616-156">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70616-156">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-157">-이란 Casesensitive</span><span class="sxs-lookup"><span data-stu-id="70616-157">-SubjectCaseSensitive</span></span>
<span data-ttu-id="70616-158">주제 필드가 대/소문자를 구분 하 여 비교 하도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-158">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="70616-159">지정 하지 않으면 제목은 대/소문자를 구분 하지 않고 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70616-159">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="70616-160">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="70616-160">-SubjectEndsWith</span></span>
<span data-ttu-id="70616-161">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-161">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="70616-162">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70616-162">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70616-163">-TopicName</span><span class="sxs-lookup"><span data-stu-id="70616-163">-TopicName</span></span>
<span data-ttu-id="70616-164">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-164">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="70616-165">-확인</span><span class="sxs-lookup"><span data-stu-id="70616-165">-Confirm</span></span>
<span data-ttu-id="70616-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70616-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70616-167">-WhatIf</span></span>
<span data-ttu-id="70616-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70616-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70616-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70616-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70616-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70616-170">-DefaultProfile</span></span>
<span data-ttu-id="70616-171">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70616-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70616-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70616-172">CommonParameters</span></span>
<span data-ttu-id="70616-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70616-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70616-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70616-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70616-175">입력</span><span class="sxs-lookup"><span data-stu-id="70616-175">INPUTS</span></span>

### <span data-ttu-id="70616-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70616-176">System.String</span></span>
<span data-ttu-id="70616-177">Microsoft. c c. c c. c c. c c. c c.</span><span class="sxs-lookup"><span data-stu-id="70616-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="70616-178">출력</span><span class="sxs-lookup"><span data-stu-id="70616-178">OUTPUTS</span></span>

### <span data-ttu-id="70616-179">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="70616-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="70616-180">상속자</span><span class="sxs-lookup"><span data-stu-id="70616-180">NOTES</span></span>

## <span data-ttu-id="70616-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70616-181">RELATED LINKS</span></span>

