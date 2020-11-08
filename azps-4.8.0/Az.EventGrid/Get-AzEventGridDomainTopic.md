---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213603"
---
# <span data-ttu-id="ec890-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ec890-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="ec890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec890-102">SYNOPSIS</span></span>
<span data-ttu-id="ec890-103">이벤트 그리드 도메인 항목의 세부 정보를 가져오거나 현재 Azure 구독의 특정 이벤트 그리드 도메인 아래에 있는 모든 이벤트 그리드 도메인 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="ec890-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec890-104">SYNTAX</span></span>

### <span data-ttu-id="ec890-105">DomainTopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec890-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec890-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec890-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec890-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec890-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec890-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ec890-108">DESCRIPTION</span></span>
<span data-ttu-id="ec890-109">Get-AzEventGridDomainTopic cmdlet은 지정 된 이벤트 그리드 도메인 항목에 대 한 세부 정보 또는 현재 Azure 구독에서 특정 도메인에 있는 모든 이벤트 그리드 도메인 항목의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="ec890-110">도메인 주제 이름을 제공 하는 경우 단일 이벤트 그리드 도메인 항목의 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="ec890-111">도메인 항목 이름이 제공 되지 않으면 지정 된 도메인 이름 아래에 있는 도메인 항목 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="ec890-112">이 목록에 반환 되는 요소 수는 Top 매개 변수를 통해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ec890-113">Top 값을 지정 하지 않거나 $null 하는 경우 목록에 모든 도메인 항목 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="ec890-114">그렇지 않으면 Top은 목록에 반환 될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ec890-115">더 많은 도메인 항목을 계속 사용할 수 있는 경우 다음에 도메인 항목의 다음 페이지를 가져오기 위해 다음 호출에서 NextLink의 값을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="ec890-116">마지막으로, ODataQuery 매개 변수를 사용 하 여 검색 결과에 대 한 필터링을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ec890-117">필터링 쿼리는 Name 속성에만 사용 하 여 OData 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ec890-118">지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ec890-119">예제의</span><span class="sxs-lookup"><span data-stu-id="ec890-119">EXAMPLES</span></span>

### <span data-ttu-id="ec890-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec890-120">Example 1</span></span>

<span data-ttu-id="ec890-121">\` \` \` \` 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1 아래 DomainTopic1 \` 이벤트 그리드 도메인 항목의 세부 정보를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="ec890-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ec890-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="ec890-122">Example 2</span></span>

<span data-ttu-id="ec890-123">\` \` \` \` \` \` ResourceId 옵션을 사용 하 여 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1 아래 DomainTopic1 이벤트 그리드 도메인 항목의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ec890-124">예제 3</span><span class="sxs-lookup"><span data-stu-id="ec890-124">Example 3</span></span>

<span data-ttu-id="ec890-125">페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 모든 이벤트 눈금 도메인 항목을 나열 \` \` \` \` 합니다 (모든 결과가 단일 샷에 반환 됨).</span><span class="sxs-lookup"><span data-stu-id="ec890-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ec890-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="ec890-126">Example 4</span></span>

<span data-ttu-id="ec890-127">\`페이지 매김을 사용 하지 않는 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1에서 모든 이벤트 그리드 도메인 항목 나열 \` \` \` (모든 결과가 단일 샷에 반환 됨) ResourceId 옵션</span><span class="sxs-lookup"><span data-stu-id="ec890-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="ec890-128">예제 5</span><span class="sxs-lookup"><span data-stu-id="ec890-128">Example 5</span></span>

<span data-ttu-id="ec890-129">\` \` \` \` 한 번에 10 개의 도메인 항목을 쿼리 하 $odataFilter를 충족 하는 리소스 그룹 MyResourceGroupName의 도메인 Domain1에서 이벤트 눈금 도메인 항목 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="ec890-130">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ec890-131">도메인 항목의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridDomainTopic 다시 호출 하 고 결과를 사용 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="ec890-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ec890-132">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="ec890-133">변수</span><span class="sxs-lookup"><span data-stu-id="ec890-133">PARAMETERS</span></span>

### <span data-ttu-id="ec890-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec890-134">-DefaultProfile</span></span>
<span data-ttu-id="ec890-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec890-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ec890-136">-DomainName</span></span>
<span data-ttu-id="ec890-137">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec890-138">-이름</span><span class="sxs-lookup"><span data-stu-id="ec890-138">-Name</span></span>
<span data-ttu-id="ec890-139">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec890-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ec890-140">-NextLink</span></span>
<span data-ttu-id="ec890-141">가져올 리소스의 다음 페이지에 대 한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="ec890-142">이 값은 추가 리소스를 계속 쿼리할 수 있는 첫 번째 Get-AzEventGrid cmdlet 호출을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ec890-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ec890-143">-ODataQuery</span></span>
<span data-ttu-id="ec890-144">목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ec890-145">현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec890-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec890-146">-ResourceGroupName</span></span>
<span data-ttu-id="ec890-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec890-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec890-148">-ResourceId</span></span>
<span data-ttu-id="ec890-149">이벤트 그리드 도메인 또는 그리드 도메인 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec890-150">-위쪽</span><span class="sxs-lookup"><span data-stu-id="ec890-150">-Top</span></span>
<span data-ttu-id="ec890-151">목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ec890-152">현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec890-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec890-153">CommonParameters</span></span>
<span data-ttu-id="ec890-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec890-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec890-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec890-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec890-156">입력</span><span class="sxs-lookup"><span data-stu-id="ec890-156">INPUTS</span></span>

### <span data-ttu-id="ec890-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec890-157">System.String</span></span>

### <span data-ttu-id="ec890-158">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ec890-158">System.Int32</span></span>

## <span data-ttu-id="ec890-159">출력</span><span class="sxs-lookup"><span data-stu-id="ec890-159">OUTPUTS</span></span>

### <span data-ttu-id="ec890-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ec890-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ec890-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="ec890-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="ec890-162">상속자</span><span class="sxs-lookup"><span data-stu-id="ec890-162">NOTES</span></span>

## <span data-ttu-id="ec890-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec890-163">RELATED LINKS</span></span>
