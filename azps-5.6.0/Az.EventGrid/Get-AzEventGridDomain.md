---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 919d8d0557fd6bb57cc826da8ac18bc71b911c62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984685"
---
# <span data-ttu-id="14c8b-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="14c8b-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="14c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="14c8b-103">Event Grid 도메인의 세부 정보를 얻거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="14c8b-104">구문</span><span class="sxs-lookup"><span data-stu-id="14c8b-104">SYNTAX</span></span>

### <span data-ttu-id="14c8b-105">ResourceGroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="14c8b-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c8b-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c8b-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c8b-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c8b-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c8b-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c8b-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c8b-109">설명</span><span class="sxs-lookup"><span data-stu-id="14c8b-109">DESCRIPTION</span></span>
<span data-ttu-id="14c8b-110">Get-AzEventGridDomain cmdlet은 지정된 Event Grid 도메인의 세부 정보 또는 현재 Azure 구독의 모든 Event Grid 도메인 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="14c8b-111">도메인 이름이 제공된 경우 단일 Event Grid 도메인의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="14c8b-112">도메인 이름이 제공되지 않은 경우 도메인 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="14c8b-113">이 목록에 반환되는 요소의 수는 Top 매개 변수에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="14c8b-114">상위 값이 지정되지 않은 경우 또는 $null 목록에는 한 번 반환된 모든 도메인 항목이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="14c8b-115">그렇지 않으면 위쪽은 목록에서 반환할 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="14c8b-116">더 많은 도메인을 계속 사용할 수 있는 경우 다음 호출에 NextLink의 값을 사용하여 도메인의 다음 페이지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="14c8b-117">마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="14c8b-118">필터링 쿼리는 Name 속성만 사용하여 OData 구문을 따르고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="14c8b-119">지원되는 작업에는 INCLUDE, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="14c8b-120">예제</span><span class="sxs-lookup"><span data-stu-id="14c8b-120">EXAMPLES</span></span>

### <span data-ttu-id="14c8b-121">예제 1</span><span class="sxs-lookup"><span data-stu-id="14c8b-121">Example 1</span></span>

<span data-ttu-id="14c8b-122">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 도메인1의 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="14c8b-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="14c8b-123">Example 2</span></span>

<span data-ttu-id="14c8b-124">ResourceId 옵션을 사용하여 리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 도메인1의 세부 \` 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="14c8b-125">예제 3</span><span class="sxs-lookup"><span data-stu-id="14c8b-125">Example 3</span></span>

<span data-ttu-id="14c8b-126">Pagination 없이 리소스 그룹 \` MyResourceGroupName의 모든 Event Grid 도메인을 나열합니다(모든 도메인은 한 번만 \` 반환)</span><span class="sxs-lookup"><span data-stu-id="14c8b-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="14c8b-127">예제 4</span><span class="sxs-lookup"><span data-stu-id="14c8b-127">Example 4</span></span>

<span data-ttu-id="14c8b-128">한 $odataFilter 쿼리를 충족하는 \` 리소스 그룹 MyResourceGroupName에 Event Grid 도메인(있는 \` 경우)을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="14c8b-129">더 많은 결과를 사용할 수 있는 경우 $result. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="14c8b-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="14c8b-130">도메인의 다음 페이지를 얻기 위해 사용자는 다시 호출해야 Get-AzEventGridDomain 결과를 사용할 수 있습니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="14c8b-131">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="14c8b-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="14c8b-132">예제 5</span><span class="sxs-lookup"><span data-stu-id="14c8b-132">Example 5</span></span>

<span data-ttu-id="14c8b-133">Pagination 없이 Azure 구독의 모든 Event Grid 도메인 나열(모든 도메인은 한 번으로 반환)</span><span class="sxs-lookup"><span data-stu-id="14c8b-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="14c8b-134">예제 6</span><span class="sxs-lookup"><span data-stu-id="14c8b-134">Example 6</span></span>

<span data-ttu-id="14c8b-135">Azure 구독에 한 $odataFilter 쿼리 20개 도메인을 충족하는 Event Grid 도메인(있는 경우)을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="14c8b-136">더 많은 결과를 사용할 수 있는 경우 $result. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="14c8b-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="14c8b-137">도메인의 다음 페이지를 얻기 위해 사용자는 다시 호출해야 Get-AzEventGridDomain 결과를 사용할 수 있습니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="14c8b-138">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="14c8b-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="14c8b-139">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14c8b-139">PARAMETERS</span></span>

### <span data-ttu-id="14c8b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c8b-140">-DefaultProfile</span></span>
<span data-ttu-id="14c8b-141">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c8b-142">-Name</span><span class="sxs-lookup"><span data-stu-id="14c8b-142">-Name</span></span>
<span data-ttu-id="14c8b-143">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-143">EventGrid domain name.</span></span>

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

### <span data-ttu-id="14c8b-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="14c8b-144">-NextLink</span></span>
<span data-ttu-id="14c8b-145">얻을 리소스의 다음 페이지에 대한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="14c8b-146">이 값은 더 많은 리소스를 계속 Get-AzEventGrid 경우 첫 번째 cmdlet 호출을 통해 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="14c8b-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="14c8b-147">-ODataQuery</span></span>
<span data-ttu-id="14c8b-148">목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="14c8b-149">필터링은 현재 Name 속성에만 허용됩니다. 지원되는 작업에는 INCLUDE, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="14c8b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c8b-150">-ResourceGroupName</span></span>
<span data-ttu-id="14c8b-151">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="14c8b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14c8b-152">-ResourceId</span></span>
<span data-ttu-id="14c8b-153">Event Grid 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="14c8b-154">-Top</span><span class="sxs-lookup"><span data-stu-id="14c8b-154">-Top</span></span>
<span data-ttu-id="14c8b-155">얻을 최대 리소스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="14c8b-156">유효한 값은 1에서 100 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="14c8b-157">상위 값이 지정되어 더 많은 결과를 계속 사용할 수 있는 경우 결과에 NextLink에서 검색할 다음 페이지에 대한 링크가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="14c8b-158">Top 값을 지정하지 않으면 리소스의 전체 목록이 한 번씩 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="14c8b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c8b-159">CommonParameters</span></span>
<span data-ttu-id="14c8b-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14c8b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c8b-161">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14c8b-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c8b-162">입력</span><span class="sxs-lookup"><span data-stu-id="14c8b-162">INPUTS</span></span>

### <span data-ttu-id="14c8b-163">System.String</span><span class="sxs-lookup"><span data-stu-id="14c8b-163">System.String</span></span>

## <span data-ttu-id="14c8b-164">출력</span><span class="sxs-lookup"><span data-stu-id="14c8b-164">OUTPUTS</span></span>

### <span data-ttu-id="14c8b-165">Microsoft.Azure.Commands.EventGrid.Models.PSD오마인</span><span class="sxs-lookup"><span data-stu-id="14c8b-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="14c8b-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="14c8b-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="14c8b-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14c8b-167">NOTES</span></span>

## <span data-ttu-id="14c8b-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14c8b-168">RELATED LINKS</span></span>
