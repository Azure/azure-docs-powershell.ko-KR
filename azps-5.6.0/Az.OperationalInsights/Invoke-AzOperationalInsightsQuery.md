---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: bdba6d4da6df49d1975e2cfd1cc6e47f6ce6d776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010288"
---
# <span data-ttu-id="c0153-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="c0153-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="c0153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0153-102">SYNOPSIS</span></span>
<span data-ttu-id="c0153-103">지정된 매개 변수에 따라 검색 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="c0153-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0153-104">SYNTAX</span></span>

### <span data-ttu-id="c0153-105">ByWorkspaceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0153-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0153-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0153-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0153-107">설명</span><span class="sxs-lookup"><span data-stu-id="c0153-107">DESCRIPTION</span></span>
<span data-ttu-id="c0153-108">**Invoke-AzOperationalInsightsQuery** cmdlet은 지정된 매개 변수에 따라 검색 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="c0153-109">반환된 개체의 메타데이터 속성에서 검색 상태에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="c0153-110">상태가 보류 중이면 검색이 완료되지 않은 다음, 결과는 보관함의 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="c0153-111">반환된 개체의 Value 속성에서 검색 결과를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="c0153-112">일반 쿼리 제한에 대한 자세한 내용은 여기를 https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0153-112">Please check detail of general query limits here: https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="c0153-113">예제</span><span class="sxs-lookup"><span data-stu-id="c0153-113">EXAMPLES</span></span>

### <span data-ttu-id="c0153-114">예제 1: 쿼리를 사용하여 검색 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="c0153-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="c0153-115">호출된 $queryResults.Results에는 쿼리의 결과 행이 모두 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="c0153-116">예제 2: $results. 배열에 대한 결과 IEnumerable</span><span class="sxs-lookup"><span data-stu-id="c0153-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="c0153-117">일부 쿼리는 매우 큰 데이터 집합이 반환될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="c0153-118">이 때문에 cmdlet의 기본 동작은 메모리 비용을 줄이기 위해 IEnumerable을 반환하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="c0153-119">결과 배열을 원할 경우 LINQ 열제 가능.ToArray() 확장 메서드를 사용하여 IEnumerable을 배열로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="c0153-120">예제 3: 특정 기간 동안 쿼리를 사용하여 검색 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="c0153-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="c0153-121">이 쿼리의 결과는 지난 24시간으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="c0153-122">예제 4: 쿼리 결과에 & 통계 포함</span><span class="sxs-lookup"><span data-stu-id="c0153-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="c0153-123">렌더링 및 통계 정보에 대한 [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) 자세한 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0153-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="c0153-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0153-124">PARAMETERS</span></span>

### <span data-ttu-id="c0153-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0153-125">-AsJob</span></span>
<span data-ttu-id="c0153-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c0153-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0153-127">-DefaultProfile</span></span>
<span data-ttu-id="c0153-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0153-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="c0153-129">-IncludeRender</span></span>
<span data-ttu-id="c0153-130">지정한 경우 메트릭 쿼리에 대한 렌더링 정보가 응답에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-130">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="c0153-131">-IncludeStatistics</span></span>
<span data-ttu-id="c0153-132">지정한 경우 쿼리 통계가 응답에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-132">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-133">-쿼리</span><span class="sxs-lookup"><span data-stu-id="c0153-133">-Query</span></span>
<span data-ttu-id="c0153-134">실행할 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-134">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="c0153-135">-Timespan</span></span>
<span data-ttu-id="c0153-136">쿼리를 에 의해 바인딩할 시간pan입니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-136">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="c0153-137">-Wait</span></span>
<span data-ttu-id="c0153-138">서버가 쿼리를 처리하는 데 소비되는 시간의 양에 상한을 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="c0153-139">다음을 참조할 수 있습니다. https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="c0153-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-140">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="c0153-140">-Workspace</span></span>
<span data-ttu-id="c0153-141">작업 영역</span><span class="sxs-lookup"><span data-stu-id="c0153-141">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="c0153-142">-WorkspaceId</span></span>
<span data-ttu-id="c0153-143">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-143">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0153-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0153-144">CommonParameters</span></span>
<span data-ttu-id="c0153-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0153-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0153-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0153-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0153-147">입력</span><span class="sxs-lookup"><span data-stu-id="c0153-147">INPUTS</span></span>

### <span data-ttu-id="c0153-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0153-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c0153-149">출력</span><span class="sxs-lookup"><span data-stu-id="c0153-149">OUTPUTS</span></span>

### <span data-ttu-id="c0153-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="c0153-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="c0153-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0153-151">NOTES</span></span>

## <span data-ttu-id="c0153-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0153-152">RELATED LINKS</span></span>
