---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529834"
---
# <span data-ttu-id="9fb52-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="9fb52-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="9fb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb52-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb52-103">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fb52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fb52-104">SYNTAX</span></span>

### <span data-ttu-id="9fb52-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9fb52-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb52-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fb52-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb52-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9fb52-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fb52-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fb52-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb52-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9fb52-109">DESCRIPTION</span></span>
<span data-ttu-id="9fb52-110">이벤트 눈금 이벤트 구독의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="9fb52-111">이를 사용 하 여 기존 이벤트 구독의 필터, 대상 또는 레이블을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="9fb52-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9fb52-112">EXAMPLES</span></span>

### <span data-ttu-id="9fb52-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fb52-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="9fb52-114">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="9fb52-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="9fb52-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9fb52-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="9fb52-116">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대 한 \` 이벤트 구독 ES1의 끝점 \` 을 다음으로 업데이트 합니다.\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="9fb52-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="9fb52-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="9fb52-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="9fb52-118">\` \` 새 끝점 as \` https://requestb.in/1kxxoui1\ ' 및 새 부분 endswith 필터를 jpg로 사용 하 여 EventHub 네임 스페이스 ContosoNamespace에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .\`</span><span class="sxs-lookup"><span data-stu-id="9fb52-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="9fb52-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="9fb52-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="9fb52-120">\` \` \` $Labels 새 레이블이 있는 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 ES1의 속성을 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="9fb52-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="9fb52-121">변수</span><span class="sxs-lookup"><span data-stu-id="9fb52-121">PARAMETERS</span></span>

### <span data-ttu-id="9fb52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb52-122">-DefaultProfile</span></span>
<span data-ttu-id="9fb52-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-124">-끝점</span><span class="sxs-lookup"><span data-stu-id="9fb52-124">-Endpoint</span></span>
<span data-ttu-id="9fb52-125">이벤트 구독 대상 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="9fb52-126">이것은 webhook URL 또는 EventHub의 Azure resource ID 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="9fb52-127">-EndpointType</span></span>
<span data-ttu-id="9fb52-128">끝점 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-128">Endpoint Type.</span></span>
<span data-ttu-id="9fb52-129">이는 webhook 또는 eventhub 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9fb52-130">-EventSubscriptionName</span></span>
<span data-ttu-id="9fb52-131">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-131">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="9fb52-132">-IncludedEventType</span></span>
<span data-ttu-id="9fb52-133">포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fb52-134">-InputObject</span></span>
<span data-ttu-id="9fb52-135">EventGridSubscription 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-136">-레이블</span><span class="sxs-lookup"><span data-stu-id="9fb52-136">-Label</span></span>
<span data-ttu-id="9fb52-137">이벤트 구독에 대 한 레이블</span><span class="sxs-lookup"><span data-stu-id="9fb52-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb52-138">-ResourceGroupName</span></span>
<span data-ttu-id="9fb52-139">주제의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fb52-140">-ResourceId</span></span>
<span data-ttu-id="9fb52-141">이벤트 구독이 만들어진 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-141">The identifier of the resource to which the event subscription was created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="9fb52-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="9fb52-143">지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="9fb52-144">지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-145">-# Endswith</span><span class="sxs-lookup"><span data-stu-id="9fb52-145">-SubjectEndsWith</span></span>
<span data-ttu-id="9fb52-146">지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="9fb52-147">지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="9fb52-148">-TopicName</span></span>
<span data-ttu-id="9fb52-149">이벤트 구독을 만들어야 하는 주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-150">-확인</span><span class="sxs-lookup"><span data-stu-id="9fb52-150">-Confirm</span></span>
<span data-ttu-id="9fb52-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb52-152">-WhatIf</span></span>
<span data-ttu-id="9fb52-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb52-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb52-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb52-155">CommonParameters</span></span>
<span data-ttu-id="9fb52-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb52-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb52-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb52-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb52-158">입력</span><span class="sxs-lookup"><span data-stu-id="9fb52-158">INPUTS</span></span>

### <span data-ttu-id="9fb52-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9fb52-159">System.String</span></span>
<span data-ttu-id="9fb52-160">Microsoft. PSEventSubscription []. 문자열 []</span><span class="sxs-lookup"><span data-stu-id="9fb52-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="9fb52-161">출력</span><span class="sxs-lookup"><span data-stu-id="9fb52-161">OUTPUTS</span></span>

### <span data-ttu-id="9fb52-162">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="9fb52-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="9fb52-163">상속자</span><span class="sxs-lookup"><span data-stu-id="9fb52-163">NOTES</span></span>

## <span data-ttu-id="9fb52-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fb52-164">RELATED LINKS</span></span>

