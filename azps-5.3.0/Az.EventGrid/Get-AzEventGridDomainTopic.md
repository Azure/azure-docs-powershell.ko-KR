---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376811"
---
# <span data-ttu-id="4cad8-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4cad8-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="4cad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cad8-102">SYNOPSIS</span></span>
<span data-ttu-id="4cad8-103">Event Grid 도메인 토픽의 세부 정보를 얻거나 현재 Azure 구독의 특정 Event Grid 도메인 아래에 있는 모든 Event Grid 도메인 토픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="4cad8-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cad8-104">SYNTAX</span></span>

### <span data-ttu-id="4cad8-105">DomainTopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4cad8-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cad8-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cad8-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cad8-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cad8-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cad8-108">설명</span><span class="sxs-lookup"><span data-stu-id="4cad8-108">DESCRIPTION</span></span>
<span data-ttu-id="4cad8-109">Get-AzEventGridDomainTopic cmdlet은 지정된 Event Grid 도메인 토픽의 세부 정보 또는 현재 Azure 구독의 특정 도메인에 있는 모든 Event Grid 도메인 토픽 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="4cad8-110">도메인 토픽 이름이 제공된 경우 단일 Event Grid 도메인 토픽의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="4cad8-111">도메인 토픽 이름이 제공되지 않으면 지정된 도메인 이름의 도메인 토픽 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="4cad8-112">이 목록에 반환되는 요소 수는 Top 매개 변수에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="4cad8-113">상위 값이 지정되지 않은 경우 $null 모든 도메인 토픽 항목이 목록에 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="4cad8-114">그렇지 않으면 맨 위가 목록에 반환될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="4cad8-115">더 많은 도메인 토픽을 계속 사용할 수 있는 경우 다음 호출에서 NextLink의 값을 사용하여 도메인 토픽의 다음 페이지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="4cad8-116">마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="4cad8-117">필터링 쿼리는 Name 속성만 사용하는 OData 구문을 따르게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="4cad8-118">지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="4cad8-119">예제</span><span class="sxs-lookup"><span data-stu-id="4cad8-119">EXAMPLES</span></span>

### <span data-ttu-id="4cad8-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="4cad8-120">Example 1</span></span>

<span data-ttu-id="4cad8-121">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Event Grid 도메인 Domain1에서 Event Grid 도메인 토픽 DomainTopic1의 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="4cad8-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="4cad8-122">Example 2</span></span>

<span data-ttu-id="4cad8-123">ResourceId 옵션을 사용하여 리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Event Grid 도메인 Domain1에서 Event Grid 도메인 토픽 DomainTopic1의 \` 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="4cad8-124">예제 3</span><span class="sxs-lookup"><span data-stu-id="4cad8-124">Example 3</span></span>

<span data-ttu-id="4cad8-125">Event Grid 도메인 도메인 1 아래에 있는 모든 Event Grid 도메인 토픽을 나열합니다( 단번에 모든 결과가 반환되는 경우) \` \` \` MyResourceGroupName 리소스 그룹에서 MyResourceGroupName을 \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="4cad8-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="4cad8-126">Example 4</span></span>

<span data-ttu-id="4cad8-127">ResourceId 옵션을 사용하여 Event Grid 도메인 도메인 1에 있는 모든 Event Grid 도메인 토픽을 \` \` 나열합니다. \` \`</span><span class="sxs-lookup"><span data-stu-id="4cad8-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="4cad8-128">예제 5</span><span class="sxs-lookup"><span data-stu-id="4cad8-128">Example 5</span></span>

<span data-ttu-id="4cad8-129">리소스 그룹 \` \` \` MyResourceGroupName의 domain Domain1 아래에 한 $odataFilter 쿼리 10개 도메인 토픽을 충족하는 Event Grid 도메인 토픽(있는 경우)을 \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="4cad8-130">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="4cad8-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="4cad8-131">도메인 토픽의 다음 페이지를 얻기 위해 사용자는 다시 호출하여 결과를 Get-AzEventGridDomainTopic 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="4cad8-132">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="4cad8-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="4cad8-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cad8-133">PARAMETERS</span></span>

### <span data-ttu-id="4cad8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cad8-134">-DefaultProfile</span></span>
<span data-ttu-id="4cad8-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cad8-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="4cad8-136">-DomainName</span></span>
<span data-ttu-id="4cad8-137">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-137">EventGrid domain name.</span></span>

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

### <span data-ttu-id="4cad8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4cad8-138">-Name</span></span>
<span data-ttu-id="4cad8-139">EventGrid 도메인 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-139">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="4cad8-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="4cad8-140">-NextLink</span></span>
<span data-ttu-id="4cad8-141">얻을 리소스의 다음 페이지에 대한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="4cad8-142">이 값은 더 많은 리소스를 계속 Get-AzEventGrid 수 있는 경우 첫 번째 Get-AzEventGrid cmdlet 호출을 통해 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="4cad8-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4cad8-143">-ODataQuery</span></span>
<span data-ttu-id="4cad8-144">목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="4cad8-145">필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="4cad8-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cad8-146">-ResourceGroupName</span></span>
<span data-ttu-id="4cad8-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-147">The name of the resource group.</span></span>

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

### <span data-ttu-id="4cad8-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cad8-148">-ResourceId</span></span>
<span data-ttu-id="4cad8-149">Event Grid 도메인 또는 Grid 도메인 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="4cad8-150">-Top</span><span class="sxs-lookup"><span data-stu-id="4cad8-150">-Top</span></span>
<span data-ttu-id="4cad8-151">목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="4cad8-152">필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="4cad8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cad8-153">CommonParameters</span></span>
<span data-ttu-id="4cad8-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cad8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cad8-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cad8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cad8-156">입력</span><span class="sxs-lookup"><span data-stu-id="4cad8-156">INPUTS</span></span>

### <span data-ttu-id="4cad8-157">System.String</span><span class="sxs-lookup"><span data-stu-id="4cad8-157">System.String</span></span>

### <span data-ttu-id="4cad8-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4cad8-158">System.Int32</span></span>

## <span data-ttu-id="4cad8-159">출력</span><span class="sxs-lookup"><span data-stu-id="4cad8-159">OUTPUTS</span></span>

### <span data-ttu-id="4cad8-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4cad8-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="4cad8-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="4cad8-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="4cad8-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cad8-162">NOTES</span></span>

## <span data-ttu-id="4cad8-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cad8-163">RELATED LINKS</span></span>
