---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194428"
---
# <span data-ttu-id="3a077-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="3a077-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="3a077-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a077-102">SYNOPSIS</span></span>
<span data-ttu-id="3a077-103">Event Grid 항목의 세부 정보를 얻거나 현재 Azure 구독의 모든 Event Grid 토픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="3a077-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a077-104">SYNTAX</span></span>

### <span data-ttu-id="3a077-105">ResourceGroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3a077-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a077-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a077-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a077-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a077-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a077-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a077-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a077-109">설명</span><span class="sxs-lookup"><span data-stu-id="3a077-109">DESCRIPTION</span></span>
<span data-ttu-id="3a077-110">Get-AzEventGridTopic cmdlet은 지정된 Event Grid 토픽의 세부 정보 또는 현재 Azure 구독의 모든 Event Grid 토픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="3a077-111">토픽 이름이 제공된 경우 단일 Event Grid 토픽의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="3a077-112">토픽 이름이 제공되지 않은 경우 토픽 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="3a077-113">이 목록에 반환되는 요소 수는 Top 매개 변수에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="3a077-114">상위 값이 지정되지 않은 경우 또는 $null 목록에 모든 토픽 항목이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="3a077-115">그렇지 않으면 맨 위가 목록에 반환될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="3a077-116">더 많은 토픽을 계속 사용할 수 있는 경우 다음 호출에서 NextLink의 값을 사용하여 항목의 다음 페이지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="3a077-117">마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="3a077-118">필터링 쿼리는 Name 속성만 사용하는 OData 구문을 따르게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="3a077-119">지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="3a077-120">예제</span><span class="sxs-lookup"><span data-stu-id="3a077-120">EXAMPLES</span></span>

### <span data-ttu-id="3a077-121">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a077-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="3a077-122">리소스 그룹 \` \` \` MyResourceGroupName의 Event Grid 항목 Topic1에 대한 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3a077-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="3a077-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="3a077-124">리소스 그룹 \` \` \` MyResourceGroupName의 Event Grid 항목 Topic1에 대한 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3a077-125">예제 3</span><span class="sxs-lookup"><span data-stu-id="3a077-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="3a077-126">리소스 그룹 \` MyResourceGroupName의 모든 Event Grid 토픽을 페이지인하지 않고 \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="3a077-127">예제 4</span><span class="sxs-lookup"><span data-stu-id="3a077-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="3a077-128">리소스 그룹 \` MyResourceGroupName의 처음 10개 Event Grid 토픽(있는 경우)을 $odataFilter \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="3a077-129">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="3a077-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="3a077-130">토픽의 다음 페이지를 얻기 위해 사용자는 다시 호출해야 Get-AzEventGridTopic 결과를 사용할 수 있습니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="3a077-131">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="3a077-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="3a077-132">예제 5</span><span class="sxs-lookup"><span data-stu-id="3a077-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="3a077-133">구독의 모든 Event Grid 토픽을 페이제이션 없이 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="3a077-134">예제 6</span><span class="sxs-lookup"><span data-stu-id="3a077-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="3a077-135">구독에서 이벤트 쿼리를 충족하는 처음 10개 Event Grid 토픽(있는 경우)$odataFilter 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="3a077-136">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="3a077-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="3a077-137">토픽의 다음 페이지를 얻기 위해 사용자는 다시 호출해야 Get-AzEventGridTopic 결과를 사용할 수 있습니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="3a077-138">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="3a077-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="3a077-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a077-139">PARAMETERS</span></span>

### <span data-ttu-id="3a077-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a077-140">-DefaultProfile</span></span>
<span data-ttu-id="3a077-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a077-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a077-142">-Name</span><span class="sxs-lookup"><span data-stu-id="3a077-142">-Name</span></span>
<span data-ttu-id="3a077-143">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a077-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="3a077-144">-NextLink</span></span>
<span data-ttu-id="3a077-145">얻을 리소스의 다음 페이지에 대한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="3a077-146">이 값은 더 많은 리소스를 계속 Get-AzEventGrid 경우 첫 번째 Get-AzEventGrid cmdlet 호출을 통해 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a077-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="3a077-147">-ODataQuery</span></span>
<span data-ttu-id="3a077-148">목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="3a077-149">필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a077-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a077-150">-ResourceGroupName</span></span>
<span data-ttu-id="3a077-151">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a077-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a077-152">-ResourceId</span></span>
<span data-ttu-id="3a077-153">Event Grid 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="3a077-154">-Top</span><span class="sxs-lookup"><span data-stu-id="3a077-154">-Top</span></span>
<span data-ttu-id="3a077-155">얻을 최대 리소스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="3a077-156">유효한 값은 1에서 100 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="3a077-157">상위 값이 지정되어 더 많은 결과를 계속 사용할 수 있는 경우 결과에 NextLink에서 검색할 다음 페이지에 대한 링크가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="3a077-158">상위 값을 지정하지 않으면 리소스의 전체 목록이 한에 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a077-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a077-159">CommonParameters</span></span>
<span data-ttu-id="3a077-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a077-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a077-161">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a077-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a077-162">입력</span><span class="sxs-lookup"><span data-stu-id="3a077-162">INPUTS</span></span>

### <span data-ttu-id="3a077-163">System.String</span><span class="sxs-lookup"><span data-stu-id="3a077-163">System.String</span></span>

### <span data-ttu-id="3a077-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3a077-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3a077-165">출력</span><span class="sxs-lookup"><span data-stu-id="3a077-165">OUTPUTS</span></span>

### <span data-ttu-id="3a077-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="3a077-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="3a077-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="3a077-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="3a077-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a077-168">NOTES</span></span>

## <span data-ttu-id="3a077-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a077-169">RELATED LINKS</span></span>
