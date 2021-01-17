---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329613"
---
# <span data-ttu-id="0e985-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0e985-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="0e985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e985-102">SYNOPSIS</span></span>
<span data-ttu-id="0e985-103">이벤트 구독의 세부 정보를 얻거나 현재 Azure 구독의 모든 이벤트 구독 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="0e985-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e985-104">SYNTAX</span></span>

### <span data-ttu-id="0e985-105">EventSubscriptionTopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e985-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e985-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e985-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e985-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e985-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e985-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e985-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e985-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e985-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e985-113">설명</span><span class="sxs-lookup"><span data-stu-id="0e985-113">DESCRIPTION</span></span>
<span data-ttu-id="0e985-114">Get-AzEventGridSubscription cmdlet은 지정된 Event Grid 구독의 세부 정보 또는 현재 Azure 구독 또는 리소스 그룹의 모든 Event Grid 구독 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="0e985-115">이벤트 구독 이름이 제공된 경우 단일 Event Grid 구독의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="0e985-116">이벤트 구독 이름이 제공되지 않은 경우 모든 이벤트 구독 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="0e985-117">이 목록에 반환되는 요소 수는 Top 매개 변수에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="0e985-118">상위 값이 지정되지 않은 경우 $null 모든 이벤트 구독 항목이 목록에 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="0e985-119">그렇지 않으면 맨 위가 목록에 반환될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="0e985-120">더 많은 이벤트 구독을 계속 사용할 수 있는 경우 다음 호출에서 NextLink의 값을 사용하여 이벤트 구독의 다음 페이지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="0e985-121">마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="0e985-122">필터링 쿼리는 Name 속성만 사용하는 OData 구문을 따르게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="0e985-123">지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="0e985-124">예제</span><span class="sxs-lookup"><span data-stu-id="0e985-124">EXAMPLES</span></span>

### <span data-ttu-id="0e985-125">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e985-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0e985-126">리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 Topic1에 대해 만든 이벤트 구독 EventSubscription1의 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0e985-127">예제 2</span><span class="sxs-lookup"><span data-stu-id="0e985-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="0e985-128">웹후크 기반 이벤트 구독인 경우 전체 엔드포인트 URL을 포함하여 리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Topic1에 대해 만든 이벤트 구독 EventSubscription1의 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="0e985-129">예제 3</span><span class="sxs-lookup"><span data-stu-id="0e985-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="0e985-130">Pagination 없이 리소스 그룹 \` \` \` MyResourceGroupName에서 Topic1에 대해 만든 모든 이벤트 구독 목록을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="0e985-131">예제 4</span><span class="sxs-lookup"><span data-stu-id="0e985-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-132">리소스 그룹 \` \` \` MyResourceGroupName에서 토픽 Topic1에 대해 만든 처음 10개 이벤트 구독(있는 경우)을 $odataFilter \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-133">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-134">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-135">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="0e985-136">예제 5</span><span class="sxs-lookup"><span data-stu-id="0e985-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0e985-137">리소스 그룹 \` \` \` MyResourceGroupName에 대해 만든 이벤트 구독 EventSubscription1의 세부 정보를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0e985-138">예제 6</span><span class="sxs-lookup"><span data-stu-id="0e985-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="0e985-139">현재 선택한 Azure 구독에 대해 만든 이벤트 구독 \` EventSubscription1의 \` 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="0e985-140">예제 7</span><span class="sxs-lookup"><span data-stu-id="0e985-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="0e985-141">Pagination 없이 리소스 그룹 \` MyResourceGroupName에서 만든 모든 전역 이벤트 구독 목록을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="0e985-142">예제 8</span><span class="sxs-lookup"><span data-stu-id="0e985-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-143">리소스 그룹 \` MyResourceGroupName에서 만든 처음 5개 이벤트 구독(있는 경우)을 $odataFilter \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-144">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-145">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-146">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="0e985-147">예제 9</span><span class="sxs-lookup"><span data-stu-id="0e985-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="0e985-148">현재 선택한 Azure 구독에서 만든 모든 전역 이벤트 구독의 목록을 페이그인하지 않고 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="0e985-149">예제 10</span><span class="sxs-lookup"><span data-stu-id="0e985-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-150">현재 선택한 Azure 구독에서 만든 처음 15개 전역 이벤트 구독(있는 경우)을 $odataFilter 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-151">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-152">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-153">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="0e985-154">예제 11</span><span class="sxs-lookup"><span data-stu-id="0e985-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="0e985-155">지정한 위치 westus2의 리소스 그룹 \` MyResourceGroupName에서 만든 모든 지역별 이벤트 구독 목록을 페이지 인하지 않고 \` \` \` 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="0e985-156">예제 12</span><span class="sxs-lookup"><span data-stu-id="0e985-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-157">리소스 그룹 \` MyResourceGroupName에서 만든 처음 15개 지역 이벤트 구독(있는 경우)을 지정된 \` 위치 westus2에 나열하여 $odataFilter \` \` 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-158">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-159">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-160">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="0e985-161">예제 13</span><span class="sxs-lookup"><span data-stu-id="0e985-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="0e985-162">지정한 EventHub 네임스페이스에 대해 만든 모든 이벤트 구독의 목록을 페이그인(pagination) 없이 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="0e985-163">예제 14</span><span class="sxs-lookup"><span data-stu-id="0e985-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-164">지정된 EventHub 네임스페이스에 대해 생성된 처음 25개 이벤트 구독(있는 경우)을 $odataFilter 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-165">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-166">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-167">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="0e985-168">예제 15</span><span class="sxs-lookup"><span data-stu-id="0e985-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="0e985-169">지정된 토픽 유형(EventHub 네임스페이스)에 대해 만든 모든 이벤트 구독의 목록을 페이제이션 없이 지정한 위치에 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="0e985-170">예제 16</span><span class="sxs-lookup"><span data-stu-id="0e985-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-171">지정된 토픽 유형(EventHub 네임스페이스)에 대해 만든 처음 15개 이벤트 구독(있는 경우)을 지정된 $odataFilter 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-172">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-173">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-174">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="0e985-175">예제 17</span><span class="sxs-lookup"><span data-stu-id="0e985-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="0e985-176">특정 리소스 그룹에 대해 만든 모든 이벤트 구독 목록을 페이게이션하지 않고 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="0e985-177">예제 18</span><span class="sxs-lookup"><span data-stu-id="0e985-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="0e985-178">특정 리소스 그룹에 대해 생성된 처음 100개 이벤트 구독(있는 경우)을 $odataFilter 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="0e985-179">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="0e985-180">이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="0e985-181">호출자는 결과 시 중지해야 합니다. NextLink가 $null.</span><span class="sxs-lookup"><span data-stu-id="0e985-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="0e985-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e985-182">PARAMETERS</span></span>

### <span data-ttu-id="0e985-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e985-183">-DefaultProfile</span></span>
<span data-ttu-id="0e985-184">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e985-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e985-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="0e985-185">-DomainInputObject</span></span>
<span data-ttu-id="0e985-186">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-186">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="0e985-187">-DomainName</span></span>
<span data-ttu-id="0e985-188">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="0e985-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="0e985-190">EventGrid 도메인 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-190">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="0e985-191">-DomainTopicName</span></span>
<span data-ttu-id="0e985-192">EventGrid 도메인 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0e985-193">-EventSubscriptionName</span></span>
<span data-ttu-id="0e985-194">이벤트 구독의 이름</span><span class="sxs-lookup"><span data-stu-id="0e985-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="0e985-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="0e985-196">이벤트 구독 대상의 전체 엔드포인트 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e985-197">-InputObject</span></span>
<span data-ttu-id="0e985-198">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="0e985-199">-Location</span><span class="sxs-lookup"><span data-stu-id="0e985-199">-Location</span></span>
<span data-ttu-id="0e985-200">위치</span><span class="sxs-lookup"><span data-stu-id="0e985-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="0e985-201">-NextLink</span></span>
<span data-ttu-id="0e985-202">얻을 리소스의 다음 페이지에 대한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="0e985-203">이 값은 더 많은 리소스를 계속 Get-AzEventGrid 수 있는 경우 첫 번째 Get-AzEventGrid cmdlet 호출을 통해 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="0e985-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0e985-204">-ODataQuery</span></span>
<span data-ttu-id="0e985-205">목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="0e985-206">필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e985-207">-ResourceGroupName</span></span>
<span data-ttu-id="0e985-208">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e985-209">-ResourceId</span></span>
<span data-ttu-id="0e985-210">이벤트 구독이 만들어진 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-210">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-211">-Top</span><span class="sxs-lookup"><span data-stu-id="0e985-211">-Top</span></span>
<span data-ttu-id="0e985-212">목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="0e985-213">필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0e985-214">-TopicName</span></span>
<span data-ttu-id="0e985-215">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="0e985-216">-TopicTypeName</span></span>
<span data-ttu-id="0e985-217">TopicType 이름</span><span class="sxs-lookup"><span data-stu-id="0e985-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e985-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e985-218">CommonParameters</span></span>
<span data-ttu-id="0e985-219">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e985-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e985-220">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e985-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e985-221">입력</span><span class="sxs-lookup"><span data-stu-id="0e985-221">INPUTS</span></span>

### <span data-ttu-id="0e985-222">System.String</span><span class="sxs-lookup"><span data-stu-id="0e985-222">System.String</span></span>

### <span data-ttu-id="0e985-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="0e985-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="0e985-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="0e985-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="0e985-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0e985-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="0e985-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0e985-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0e985-227">출력</span><span class="sxs-lookup"><span data-stu-id="0e985-227">OUTPUTS</span></span>

### <span data-ttu-id="0e985-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="0e985-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0e985-229">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e985-229">NOTES</span></span>

## <span data-ttu-id="0e985-230">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e985-230">RELATED LINKS</span></span>
