---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700862"
---
# <span data-ttu-id="2870e-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2870e-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="2870e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2870e-102">SYNOPSIS</span></span>
<span data-ttu-id="2870e-103">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="2870e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2870e-104">SYNTAX</span></span>

### <span data-ttu-id="2870e-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2870e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2870e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2870e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2870e-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2870e-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2870e-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2870e-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2870e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2870e-109">DESCRIPTION</span></span>
<span data-ttu-id="2870e-110">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="2870e-111">이를 사용 하 여 기존 이벤트 구독의 필터, 대상 또는 레이블을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="2870e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2870e-112">EXAMPLES</span></span>

### <span data-ttu-id="2870e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="2870e-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="2870e-114">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="2870e-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="2870e-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="2870e-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="2870e-116">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="2870e-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="2870e-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="2870e-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="2870e-118">\` \` 새 끝점 as \` https://requestb.in/1kxxoui1\ ' 및 새 부분 endswith 필터를 jpg로 사용 하 여 EventHub 네임 스페이스 ContosoNamespace에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .\`</span><span class="sxs-lookup"><span data-stu-id="2870e-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="2870e-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="2870e-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="2870e-120">\` \` \` $Labels 새 레이블이 있는 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="2870e-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="2870e-121">변수</span><span class="sxs-lookup"><span data-stu-id="2870e-121">PARAMETERS</span></span>

### <span data-ttu-id="2870e-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="2870e-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="2870e-123">배달 되지 않은 이벤트를 저장 하는 데 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="2870e-124">저장소 blob 컨테이너의 Azure 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="2870e-125">예:/subscriptions/[SubscriptionId]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="2870e-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="2870e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2870e-126">-DefaultProfile</span></span>
<span data-ttu-id="2870e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2870e-128">-끝점</span><span class="sxs-lookup"><span data-stu-id="2870e-128">-Endpoint</span></span>
<span data-ttu-id="2870e-129">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="2870e-130">이는 webhook URL 또는 EventHub, storage queue 또는 hybridconnection의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="2870e-131">예를 들어 하이브리드 연결의 리소스 ID에는/subscriptions/[Azure 구독 ID]/Resource그룹/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName] 형식이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="2870e-132">이벤트 그리드 cmdlet을 실행 하기 전에 대상 끝점을 만들어 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="2870e-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="2870e-133">-EndpointType</span></span>
<span data-ttu-id="2870e-134">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-134">Endpoint Type.</span></span>
<span data-ttu-id="2870e-135">이는 webhook, eventhub, storagequeue 또는 hybridconnection 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="2870e-136">기본값은 webhook입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2870e-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2870e-137">-EventSubscriptionName</span></span>
<span data-ttu-id="2870e-138">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-138">The name of the event subscription</span></span>

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

### <span data-ttu-id="2870e-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="2870e-139">-EventTtl</span></span>
<span data-ttu-id="2870e-140">이벤트 배달을 위한 시간 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="2870e-141">이 값은 1에서 1440 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-141">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="2870e-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="2870e-142">-IncludedEventType</span></span>
<span data-ttu-id="2870e-143">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="2870e-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2870e-144">-InputObject</span></span>
<span data-ttu-id="2870e-145">EventGridSubscription 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-145">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="2870e-146">-레이블</span><span class="sxs-lookup"><span data-stu-id="2870e-146">-Label</span></span>
<span data-ttu-id="2870e-147">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="2870e-147">Labels for the event subscription</span></span>

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

### <span data-ttu-id="2870e-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="2870e-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="2870e-149">이벤트 배달을 위한 최대 시도 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="2870e-150">이 값은 1에서 30 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-150">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="2870e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2870e-151">-ResourceGroupName</span></span>
<span data-ttu-id="2870e-152">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2870e-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2870e-153">-ResourceId</span></span>
<span data-ttu-id="2870e-154">이벤트 구독이 만들어진 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="2870e-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="2870e-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="2870e-156">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="2870e-157">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-157">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="2870e-158">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="2870e-158">-SubjectEndsWith</span></span>
<span data-ttu-id="2870e-159">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="2870e-160">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-160">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="2870e-161">-TopicName</span><span class="sxs-lookup"><span data-stu-id="2870e-161">-TopicName</span></span>
<span data-ttu-id="2870e-162">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-162">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="2870e-163">-확인</span><span class="sxs-lookup"><span data-stu-id="2870e-163">-Confirm</span></span>
<span data-ttu-id="2870e-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2870e-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2870e-165">-WhatIf</span></span>
<span data-ttu-id="2870e-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2870e-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2870e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2870e-168">CommonParameters</span></span>
<span data-ttu-id="2870e-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2870e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2870e-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2870e-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2870e-171">입력</span><span class="sxs-lookup"><span data-stu-id="2870e-171">INPUTS</span></span>

### <span data-ttu-id="2870e-172">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2870e-172">System.String</span></span>

### <span data-ttu-id="2870e-173">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="2870e-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="2870e-174">출력</span><span class="sxs-lookup"><span data-stu-id="2870e-174">OUTPUTS</span></span>

### <span data-ttu-id="2870e-175">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="2870e-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="2870e-176">상속자</span><span class="sxs-lookup"><span data-stu-id="2870e-176">NOTES</span></span>

## <span data-ttu-id="2870e-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2870e-177">RELATED LINKS</span></span>
