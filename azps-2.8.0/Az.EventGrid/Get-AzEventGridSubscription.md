---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696536"
---
# <span data-ttu-id="8fa22-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8fa22-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="8fa22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa22-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa22-103">이벤트 구독에 대 한 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="8fa22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8fa22-104">SYNTAX</span></span>

### <span data-ttu-id="8fa22-105">EventSubscriptionTopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8fa22-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fa22-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa22-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fa22-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa22-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fa22-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fa22-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fa22-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fa22-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa22-113">설명은</span><span class="sxs-lookup"><span data-stu-id="8fa22-113">DESCRIPTION</span></span>
<span data-ttu-id="8fa22-114">Get-AzEventGridSubscription cmdlet은 지정 된 이벤트 그리드 구독에 대 한 세부 정보 또는 현재 Azure 구독 또는 리소스 그룹에 있는 모든 이벤트 그리드 구독 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="8fa22-115">이벤트 구독 이름을 제공 하는 경우 단일 이벤트 그리드 구독에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="8fa22-116">이벤트 구독 이름을 제공 하지 않으면 모든 이벤트 구독 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="8fa22-117">이 목록에 반환 되는 요소 수는 Top 매개 변수를 통해 제어 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="8fa22-118">Top 값을 지정 하지 않거나 $null 하는 경우 목록에 모든 이벤트 구독 항목이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="8fa22-119">그렇지 않으면 Top은 목록에 반환 될 최대 요소 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="8fa22-120">더 많은 이벤트 구독을 사용할 수 있는 경우 다음에 이벤트 구독의 다음 페이지를 가져오려면 다음 호출에서 NextLink의 값을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="8fa22-121">마지막으로, ODataQuery 매개 변수를 사용 하 여 검색 결과에 대 한 필터링을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="8fa22-122">필터링 쿼리는 Name 속성에만 사용 하 여 OData 구문을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="8fa22-123">지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="8fa22-124">예제의</span><span class="sxs-lookup"><span data-stu-id="8fa22-124">EXAMPLES</span></span>

### <span data-ttu-id="8fa22-125">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fa22-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8fa22-126">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대해 생성 \` 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="8fa22-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8fa22-127">예제 2</span><span class="sxs-lookup"><span data-stu-id="8fa22-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="8fa22-128">\` \` \` \` \` \` Webhook 기반 이벤트 구독 인 경우 전체 끝점 URL을 포함 하 여 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대해 생성 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="8fa22-129">예제 3</span><span class="sxs-lookup"><span data-stu-id="8fa22-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="8fa22-130">\` \` \` 페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대해 생성 된 모든 이벤트 구독의 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="8fa22-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="8fa22-131">예제 4</span><span class="sxs-lookup"><span data-stu-id="8fa22-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-132">\` \` \` \` $OdataFilter 쿼리를 충족 하는 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대해 생성 된 처음 10 개의 이벤트 구독 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-133">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-134">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-135">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8fa22-136">예제 5</span><span class="sxs-lookup"><span data-stu-id="8fa22-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8fa22-137">\` \` 리소스 그룹 MyResourceGroupName에 대해 생성 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="8fa22-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8fa22-138">예제 6</span><span class="sxs-lookup"><span data-stu-id="8fa22-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8fa22-139">\` \` 현재 선택 된 Azure 구독에 대해 생성 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="8fa22-140">예제 7</span><span class="sxs-lookup"><span data-stu-id="8fa22-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="8fa22-141">\`페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName에서 만든 모든 전역 이벤트 구독의 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="8fa22-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="8fa22-142">예제 8</span><span class="sxs-lookup"><span data-stu-id="8fa22-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-143">\` \` $OdataFilter 쿼리를 만족 하는 리소스 그룹 MyResourceGroupName에서 만든 처음 5 개의 이벤트 구독 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-144">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-145">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-146">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8fa22-147">예제 9</span><span class="sxs-lookup"><span data-stu-id="8fa22-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="8fa22-148">페이지 매김을 사용 하지 않고 현재 선택 된 Azure 구독에서 만들어진 모든 전역 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="8fa22-149">예제 10</span><span class="sxs-lookup"><span data-stu-id="8fa22-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-150">$OdataFilter 쿼리를 충족 하는 현재 선택 된 Azure 구독에서 만든 첫 15 개의 전역 이벤트 구독 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-151">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-152">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-153">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8fa22-154">예제 11</span><span class="sxs-lookup"><span data-stu-id="8fa22-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="8fa22-155">\` \` 지정 된 위치 \` westus2에서 페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName에 만든 모든 지역 이벤트 구독의 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="8fa22-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="8fa22-156">예제 12</span><span class="sxs-lookup"><span data-stu-id="8fa22-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-157">\` \` \` \` $OdataFilter 쿼리를 만족 하는 지정 된 위치 westus2에서 리소스 그룹 MyResourceGroupName에 생성 된 처음 15 개의 지역 이벤트 구독 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-158">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-159">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-160">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8fa22-161">예제 13</span><span class="sxs-lookup"><span data-stu-id="8fa22-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="8fa22-162">페이지 매김을 사용 하지 않고 지정 된 EventHub 네임 스페이스에 대해 생성 된 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="8fa22-163">예제 14</span><span class="sxs-lookup"><span data-stu-id="8fa22-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-164">$OdataFilter 쿼리를 충족 하는 지정 된 EventHub 네임 스페이스에 대해 생성 된 첫 25 개 이벤트 구독 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-165">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-166">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-167">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8fa22-168">예제 15</span><span class="sxs-lookup"><span data-stu-id="8fa22-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="8fa22-169">페이지 매김을 사용 하지 않고 지정 된 항목 형식 (EventHub 네임 스페이스)에 대해 만든 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="8fa22-170">예제 16</span><span class="sxs-lookup"><span data-stu-id="8fa22-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-171">지정 된 주제 유형 (EventHub 네임 스페이스)에 대해 생성 된 첫 번째 15 개의 이벤트 구독 ((있는 경우)을 $odataFilter 쿼리를 만족 하는 지정 된 위치에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-172">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-173">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-174">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8fa22-175">예제 17</span><span class="sxs-lookup"><span data-stu-id="8fa22-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="8fa22-176">페이지 매김을 사용 하지 않고 특정 리소스 그룹에 대해 만든 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="8fa22-177">예제 18</span><span class="sxs-lookup"><span data-stu-id="8fa22-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="8fa22-178">$OdataFilter 쿼리를 만족 하는 특정 리소스 그룹에 대해 생성 된 첫 번째 100 이벤트 구독 (있는 경우)을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8fa22-179">더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8fa22-180">이벤트 구독의 다음 페이지를 가져오려면 사용자가 Get-AzEventGridSubscription 다시 호출 하 여 결과를 사용 해야 합니다. 이전 통화에서 얻은 NextLink.</span><span class="sxs-lookup"><span data-stu-id="8fa22-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8fa22-181">호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="8fa22-182">변수</span><span class="sxs-lookup"><span data-stu-id="8fa22-182">PARAMETERS</span></span>

### <span data-ttu-id="8fa22-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa22-183">-DefaultProfile</span></span>
<span data-ttu-id="8fa22-184">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8fa22-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fa22-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="8fa22-185">-DomainInputObject</span></span>
<span data-ttu-id="8fa22-186">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="8fa22-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8fa22-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="8fa22-187">-DomainName</span></span>
<span data-ttu-id="8fa22-188">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="8fa22-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="8fa22-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="8fa22-190">EventGrid 도메인 주제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="8fa22-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="8fa22-191">-DomainTopicName</span></span>
<span data-ttu-id="8fa22-192">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="8fa22-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8fa22-193">-EventSubscriptionName</span></span>
<span data-ttu-id="8fa22-194">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa22-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="8fa22-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="8fa22-196">이벤트 구독 대상의 전체 끝점 URL을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="8fa22-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fa22-197">-InputObject</span></span>
<span data-ttu-id="8fa22-198">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="8fa22-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="8fa22-199">-위치</span><span class="sxs-lookup"><span data-stu-id="8fa22-199">-Location</span></span>
<span data-ttu-id="8fa22-200">Location</span><span class="sxs-lookup"><span data-stu-id="8fa22-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa22-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="8fa22-201">-NextLink</span></span>
<span data-ttu-id="8fa22-202">가져올 리소스의 다음 페이지에 대 한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="8fa22-203">이 값은 추가 리소스를 계속 쿼리할 수 있는 첫 번째 Get-AzEventGrid cmdlet 호출을 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="8fa22-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8fa22-204">-ODataQuery</span></span>
<span data-ttu-id="8fa22-205">목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="8fa22-206">현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="8fa22-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa22-207">-ResourceGroupName</span></span>
<span data-ttu-id="8fa22-208">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa22-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fa22-209">-ResourceId</span></span>
<span data-ttu-id="8fa22-210">이벤트 구독이 생성 된 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="8fa22-211">-위쪽</span><span class="sxs-lookup"><span data-stu-id="8fa22-211">-Top</span></span>
<span data-ttu-id="8fa22-212">목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="8fa22-213">현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="8fa22-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8fa22-214">-TopicName</span></span>
<span data-ttu-id="8fa22-215">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa22-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="8fa22-216">-TopicTypeName</span></span>
<span data-ttu-id="8fa22-217">TopicType 이름</span><span class="sxs-lookup"><span data-stu-id="8fa22-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa22-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa22-218">CommonParameters</span></span>
<span data-ttu-id="8fa22-219">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa22-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa22-220">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa22-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa22-221">입력</span><span class="sxs-lookup"><span data-stu-id="8fa22-221">INPUTS</span></span>

### <span data-ttu-id="8fa22-222">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8fa22-222">System.String</span></span>

### <span data-ttu-id="8fa22-223">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="8fa22-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8fa22-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8fa22-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="8fa22-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8fa22-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="8fa22-226">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="8fa22-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8fa22-227">출력</span><span class="sxs-lookup"><span data-stu-id="8fa22-227">OUTPUTS</span></span>

### <span data-ttu-id="8fa22-228">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="8fa22-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="8fa22-229">상속자</span><span class="sxs-lookup"><span data-stu-id="8fa22-229">NOTES</span></span>

## <span data-ttu-id="8fa22-230">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fa22-230">RELATED LINKS</span></span>
