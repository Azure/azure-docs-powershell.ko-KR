---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215479"
---
# <span data-ttu-id="82e2e-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="82e2e-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="82e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="82e2e-103">이벤트 그리드 도메인의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 그리드 도메인의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="82e2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82e2e-104">SYNTAX</span></span>

### <span data-ttu-id="82e2e-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="82e2e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82e2e-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e2e-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82e2e-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e2e-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82e2e-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="82e2e-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e2e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="82e2e-109">DESCRIPTION</span></span>
<span data-ttu-id="82e2e-110">Get-AzEventGridDomain cmdlet은 지정 된 이벤트 그리드 도메인의 세부 정보 또는 현재 Azure 구독에 있는 모든 이벤트 그리드 도메인의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="82e2e-111">도메인 이름이 제공 되 면 단일 이벤트 그리드 도메인의 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="82e2e-112">도메인 이름이 제공 되지 않으면 도메인 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="82e2e-113">이 목록에 반환 되는 요소 수는 Top 매개 변수를 통해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="82e2e-114">Top 값을 지정 하지 않거나 $null 하는 경우 목록에는 한 번에 반환 된 모든 도메인 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="82e2e-115">그렇지 않으면 Top은 목록에 반환 될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="82e2e-116">계속 사용할 수 있는 도메인이 더 있으면 다음 호출에서 도메인의 다음 페이지를 가져오기 위해 NextLink의 값을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="82e2e-117">마지막으로, ODataQuery 매개 변수를 사용 하 여 검색 결과에 대 한 필터링을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="82e2e-118">필터링 쿼리는 Name 속성에만 사용 하 여 OData 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="82e2e-119">지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="82e2e-120">예제의</span><span class="sxs-lookup"><span data-stu-id="82e2e-120">EXAMPLES</span></span>

### <span data-ttu-id="82e2e-121">예제 1</span><span class="sxs-lookup"><span data-stu-id="82e2e-121">Example 1</span></span>

<span data-ttu-id="82e2e-122">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="82e2e-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="82e2e-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="82e2e-123">Example 2</span></span>

<span data-ttu-id="82e2e-124">\` \` \` \` ResourceId 옵션을 사용 하 여 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="82e2e-125">예제 3</span><span class="sxs-lookup"><span data-stu-id="82e2e-125">Example 3</span></span>

<span data-ttu-id="82e2e-126">페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName의 모든 이벤트 그리드 도메인 나열 \` \` (모든 도메인이 하나의 샷에 반환 됨)</span><span class="sxs-lookup"><span data-stu-id="82e2e-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="82e2e-127">예제 4</span><span class="sxs-lookup"><span data-stu-id="82e2e-127">Example 4</span></span>

<span data-ttu-id="82e2e-128">\` \` 한 번에 10 개의 도메인을 쿼리 하 $odataFilter를 만족 하는 이벤트 그리드 도메인 (있는 경우)을 리소스 그룹 MyResourceGroupName에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="82e2e-129">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="82e2e-130">도메인의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridDomain를 다시 호출 하 고 결과를 사용 하는 것으로 예상 됩니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="82e2e-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="82e2e-131">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="82e2e-132">예제 5</span><span class="sxs-lookup"><span data-stu-id="82e2e-132">Example 5</span></span>

<span data-ttu-id="82e2e-133">페이지 매김을 사용 하지 않고 Azure 구독에 모든 이벤트 그리드 도메인 나열 (모든 도메인이 한 번에 반환 됨)</span><span class="sxs-lookup"><span data-stu-id="82e2e-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="82e2e-134">예제 6</span><span class="sxs-lookup"><span data-stu-id="82e2e-134">Example 6</span></span>

<span data-ttu-id="82e2e-135">Azure 구독에서 한 번에 20 개의 도메인을 쿼리 하는 $odataFilter를 만족 하는 이벤트 그리드 도메인 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="82e2e-136">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="82e2e-137">도메인의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridDomain를 다시 호출 하 고 결과를 사용 하는 것으로 예상 됩니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="82e2e-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="82e2e-138">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="82e2e-139">변수</span><span class="sxs-lookup"><span data-stu-id="82e2e-139">PARAMETERS</span></span>

### <span data-ttu-id="82e2e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e2e-140">-DefaultProfile</span></span>
<span data-ttu-id="82e2e-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82e2e-142">-이름</span><span class="sxs-lookup"><span data-stu-id="82e2e-142">-Name</span></span>
<span data-ttu-id="82e2e-143">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e2e-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="82e2e-144">-NextLink</span></span>
<span data-ttu-id="82e2e-145">가져올 리소스의 다음 페이지에 대 한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="82e2e-146">이 값은 추가 리소스를 계속 쿼리할 수 있는 첫 번째 Get-AzEventGrid cmdlet 호출을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="82e2e-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="82e2e-147">-ODataQuery</span></span>
<span data-ttu-id="82e2e-148">목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="82e2e-149">현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e2e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82e2e-150">-ResourceGroupName</span></span>
<span data-ttu-id="82e2e-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e2e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82e2e-152">-ResourceId</span></span>
<span data-ttu-id="82e2e-153">이벤트 그리드 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="82e2e-154">-위쪽</span><span class="sxs-lookup"><span data-stu-id="82e2e-154">-Top</span></span>
<span data-ttu-id="82e2e-155">얻을 수 있는 최대 리소스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="82e2e-156">유효한 값은 1 ~ 100입니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="82e2e-157">Top 값이 지정 되 고 더 많은 결과를 사용할 수 있는 경우 결과에는 NextLink에서 쿼리할 다음 페이지에 대 한 링크가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="82e2e-158">Top 값을 지정 하지 않으면 전체 리소스 목록이 한 번에 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82e2e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e2e-159">CommonParameters</span></span>
<span data-ttu-id="82e2e-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82e2e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e2e-161">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82e2e-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e2e-162">입력</span><span class="sxs-lookup"><span data-stu-id="82e2e-162">INPUTS</span></span>

### <span data-ttu-id="82e2e-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82e2e-163">System.String</span></span>

## <span data-ttu-id="82e2e-164">출력</span><span class="sxs-lookup"><span data-stu-id="82e2e-164">OUTPUTS</span></span>

### <span data-ttu-id="82e2e-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="82e2e-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="82e2e-166">OmainListInstance Microsoft.Azure.Commands.EventGrid.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="82e2e-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="82e2e-167">상속자</span><span class="sxs-lookup"><span data-stu-id="82e2e-167">NOTES</span></span>

## <span data-ttu-id="82e2e-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82e2e-168">RELATED LINKS</span></span>
