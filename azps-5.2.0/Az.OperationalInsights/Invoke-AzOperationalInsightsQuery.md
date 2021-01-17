---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356651"
---
# <span data-ttu-id="7fe60-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="7fe60-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="7fe60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fe60-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe60-103">지정된 매개 변수에 따라 검색 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="7fe60-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fe60-104">SYNTAX</span></span>

### <span data-ttu-id="7fe60-105">ByWorkspaceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="7fe60-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fe60-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7fe60-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fe60-107">설명</span><span class="sxs-lookup"><span data-stu-id="7fe60-107">DESCRIPTION</span></span>
<span data-ttu-id="7fe60-108">**Invoke-AzOperationalInsightsQuery** cmdlet은 지정된 매개 변수를 기반으로 검색 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="7fe60-109">반환된 개체의 메타데이터 속성에서 검색 상태에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="7fe60-110">상태가 보류 중이면 검색이 완료되지 않은 것입니다. 그러면 보관함에서 결과가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="7fe60-111">반환된 개체의 Value 속성에서 검색 결과를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="7fe60-112">일반적인 쿼리 제한에 대한 자세한 내용은 다음을 https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7fe60-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="7fe60-113">예제</span><span class="sxs-lookup"><span data-stu-id="7fe60-113">EXAMPLES</span></span>

### <span data-ttu-id="7fe60-114">예제 1: 쿼리를 사용하여 검색 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="7fe60-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="7fe60-115">호출된 후 $queryResults.Results에는 쿼리의 결과 행이 모두 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="7fe60-116">예제 2: $results. 배열에 대한 결과 IEnumerable</span><span class="sxs-lookup"><span data-stu-id="7fe60-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="7fe60-117">일부 쿼리는 매우 큰 데이터 집합이 반환될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="7fe60-118">이 때문에 cmdlet의 기본 동작은 메모리 비용을 줄이기 위해 IEnumerable을 반환하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="7fe60-119">결과 배열을 원할 경우 LINQ 열결.ToArray() 확장 메서드를 사용하여 IEnumerable을 배열로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="7fe60-120">예제 3: 특정 기간 동안 쿼리를 사용하여 검색 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="7fe60-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="7fe60-121">이 쿼리의 결과는 지난 24시간으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="7fe60-122">예제 4: 쿼리 결과에 & 통계 포함</span><span class="sxs-lookup"><span data-stu-id="7fe60-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="7fe60-123">렌더링 [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) 및 통계 정보에 대한 자세한 내용을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7fe60-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="7fe60-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fe60-124">PARAMETERS</span></span>

### <span data-ttu-id="7fe60-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fe60-125">-AsJob</span></span>
<span data-ttu-id="7fe60-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7fe60-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fe60-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe60-127">-DefaultProfile</span></span>
<span data-ttu-id="7fe60-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fe60-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="7fe60-129">-IncludeRender</span></span>
<span data-ttu-id="7fe60-130">지정된 경우 메트릭 쿼리에 대한 렌더링 정보가 응답에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-130">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="7fe60-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="7fe60-131">-IncludeStatistics</span></span>
<span data-ttu-id="7fe60-132">지정된 경우 쿼리 통계가 응답에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-132">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="7fe60-133">-Query</span><span class="sxs-lookup"><span data-stu-id="7fe60-133">-Query</span></span>
<span data-ttu-id="7fe60-134">실행할 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-134">The query to execute.</span></span>

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

### <span data-ttu-id="7fe60-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="7fe60-135">-Timespan</span></span>
<span data-ttu-id="7fe60-136">쿼리를 바인딩할 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-136">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="7fe60-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="7fe60-137">-Wait</span></span>
<span data-ttu-id="7fe60-138">서버가 쿼리를 처리하는 데 소비하는 시간의 상한을 넣습니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="7fe60-139">다음을 참조할 수 있습니다. https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="7fe60-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="7fe60-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="7fe60-140">-Workspace</span></span>
<span data-ttu-id="7fe60-141">작업 영역</span><span class="sxs-lookup"><span data-stu-id="7fe60-141">The workspace</span></span>

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

### <span data-ttu-id="7fe60-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7fe60-142">-WorkspaceId</span></span>
<span data-ttu-id="7fe60-143">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-143">The workspace ID.</span></span>

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

### <span data-ttu-id="7fe60-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe60-144">CommonParameters</span></span>
<span data-ttu-id="7fe60-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fe60-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe60-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7fe60-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe60-147">입력</span><span class="sxs-lookup"><span data-stu-id="7fe60-147">INPUTS</span></span>

### <span data-ttu-id="7fe60-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7fe60-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="7fe60-149">출력</span><span class="sxs-lookup"><span data-stu-id="7fe60-149">OUTPUTS</span></span>

### <span data-ttu-id="7fe60-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="7fe60-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="7fe60-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fe60-151">NOTES</span></span>

## <span data-ttu-id="7fe60-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fe60-152">RELATED LINKS</span></span>
