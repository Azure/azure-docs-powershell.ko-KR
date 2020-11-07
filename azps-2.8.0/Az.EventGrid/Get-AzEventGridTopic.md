---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2bae39bb6a3e0c08a86118ce9ed8f9c6fadf82c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696533"
---
# <span data-ttu-id="539be-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="539be-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="539be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="539be-102">SYNOPSIS</span></span>
<span data-ttu-id="539be-103">이벤트 그리드 항목의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 그리드 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="539be-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="539be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="539be-104">SYNTAX</span></span>

### <span data-ttu-id="539be-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="539be-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="539be-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="539be-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="539be-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="539be-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="539be-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="539be-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539be-109">설명은</span><span class="sxs-lookup"><span data-stu-id="539be-109">DESCRIPTION</span></span>
<span data-ttu-id="539be-110">Get-AzEventGridTopic cmdlet은 지정 된 이벤트 그리드 주제에 대 한 세부 정보 또는 현재 Azure 구독에 있는 모든 이벤트 그리드 항목의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="539be-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="539be-111">주제 이름을 제공 하는 경우 단일 이벤트 그리드 주제에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="539be-112">주제 이름을 제공 하지 않으면 항목 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="539be-113">이 목록에 반환 되는 요소 수는 Top 매개 변수를 통해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="539be-114">Top 값을 지정 하지 않거나 $null 하는 경우 목록에 모든 항목 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="539be-115">그렇지 않으면 Top은 목록에 반환 될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="539be-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="539be-116">더 많은 항목을 사용할 수 있는 경우 다음에 항목의 다음 페이지를 가져오려면 다음 호출에서 NextLink의 값을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="539be-117">마지막으로, ODataQuery 매개 변수를 사용 하 여 검색 결과에 대 한 필터링을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="539be-118">필터링 쿼리는 Name 속성에만 사용 하 여 OData 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="539be-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="539be-119">지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="539be-120">예제의</span><span class="sxs-lookup"><span data-stu-id="539be-120">EXAMPLES</span></span>

### <span data-ttu-id="539be-121">예제 1</span><span class="sxs-lookup"><span data-stu-id="539be-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="539be-122">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1에 대 한 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="539be-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="539be-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="539be-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="539be-124">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1에 대 한 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="539be-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="539be-125">예제 3</span><span class="sxs-lookup"><span data-stu-id="539be-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="539be-126">페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName의 모든 이벤트 눈금 항목을 나열 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="539be-127">예제 4</span><span class="sxs-lookup"><span data-stu-id="539be-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="539be-128">\` \` $OdataFilter 쿼리를 만족 하는 리소스 그룹 MyResourceGroupName 처음 10 개의 이벤트 표 항목 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="539be-129">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="539be-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="539be-130">항목의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridTopic 다시 호출 하 고 결과를 사용 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="539be-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="539be-131">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="539be-132">예제 5</span><span class="sxs-lookup"><span data-stu-id="539be-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="539be-133">페이지 매김을 사용 하지 않고 구독에 모든 이벤트 눈금 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="539be-134">예제 6</span><span class="sxs-lookup"><span data-stu-id="539be-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="539be-135">구독에서 $odataFilter 쿼리를 충족 하는 처음 10 개의 이벤트 그리드 항목 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="539be-136">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="539be-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="539be-137">항목의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridTopic 다시 호출 하 고 결과를 사용 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="539be-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="539be-138">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="539be-139">변수</span><span class="sxs-lookup"><span data-stu-id="539be-139">PARAMETERS</span></span>

### <span data-ttu-id="539be-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539be-140">-DefaultProfile</span></span>
<span data-ttu-id="539be-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="539be-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="539be-142">-이름</span><span class="sxs-lookup"><span data-stu-id="539be-142">-Name</span></span>
<span data-ttu-id="539be-143">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="539be-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="539be-144">-NextLink</span></span>
<span data-ttu-id="539be-145">가져올 리소스의 다음 페이지에 대 한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="539be-146">이 값은 추가 리소스를 계속 쿼리할 수 있는 첫 번째 Get-AzEventGrid cmdlet 호출을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="539be-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="539be-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="539be-147">-ODataQuery</span></span>
<span data-ttu-id="539be-148">목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="539be-149">현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="539be-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="539be-150">-ResourceGroupName</span></span>
<span data-ttu-id="539be-151">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="539be-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="539be-152">-ResourceId</span></span>
<span data-ttu-id="539be-153">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="539be-154">-위쪽</span><span class="sxs-lookup"><span data-stu-id="539be-154">-Top</span></span>
<span data-ttu-id="539be-155">얻을 수 있는 최대 리소스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="539be-156">유효한 값은 1 ~ 100입니다.</span><span class="sxs-lookup"><span data-stu-id="539be-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="539be-157">Top 값이 지정 되 고 더 많은 결과를 사용할 수 있는 경우 결과에는 NextLink에서 쿼리할 다음 페이지에 대 한 링크가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="539be-158">Top 값을 지정 하지 않으면 전체 리소스 목록이 한 번에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="539be-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="539be-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539be-159">CommonParameters</span></span>
<span data-ttu-id="539be-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="539be-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539be-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539be-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539be-162">입력</span><span class="sxs-lookup"><span data-stu-id="539be-162">INPUTS</span></span>

### <span data-ttu-id="539be-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="539be-163">System.String</span></span>

### <span data-ttu-id="539be-164">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="539be-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="539be-165">출력</span><span class="sxs-lookup"><span data-stu-id="539be-165">OUTPUTS</span></span>

### <span data-ttu-id="539be-166">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="539be-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="539be-167">Microsoft. Azure.. m a g. 모델.</span><span class="sxs-lookup"><span data-stu-id="539be-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="539be-168">상속자</span><span class="sxs-lookup"><span data-stu-id="539be-168">NOTES</span></span>

## <span data-ttu-id="539be-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="539be-169">RELATED LINKS</span></span>
