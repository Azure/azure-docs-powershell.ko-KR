---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527995"
---
# <span data-ttu-id="a45a8-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="a45a8-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="a45a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a45a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a45a8-103">지정 된 매개 변수를 기준으로 검색 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a45a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a45a8-104">SYNTAX</span></span>

### <span data-ttu-id="a45a8-105">ByWorkspaceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="a45a8-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a45a8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a45a8-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a45a8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a45a8-107">DESCRIPTION</span></span>
<span data-ttu-id="a45a8-108">**AzureRmOperationalInsightsQuery** cmdlet은 지정 된 매개 변수를 기준으로 검색 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>

<span data-ttu-id="a45a8-109">반환 된 개체의 Metadata 속성에서 검색 상태에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="a45a8-110">상태가 보류 중 이면 검색이 완료 되지 않은 것 이며 결과는 보관 파일에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>

<span data-ttu-id="a45a8-111">반환 된 개체의 Value 속성에서 검색 결과를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="a45a8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a45a8-112">EXAMPLES</span></span>

### <span data-ttu-id="a45a8-113">예제 1: 쿼리를 사용 하 여 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="a45a8-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="a45a8-114">호출 되 면 $queryResults에 쿼리 결과의 모든 행이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="a45a8-115">예제 2: $results 변환 배열로 IEnumberable 결과</span><span class="sxs-lookup"><span data-stu-id="a45a8-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="a45a8-116">일부 쿼리에서는 매우 큰 데이터 집합이 반환 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="a45a8-117">이 때문에 cmdlet의 기본 동작은 메모리 비용을 줄이기 위해 IEnumerable을 반환 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="a45a8-118">결과 배열을 만들려면 LINQ Enumerable () 확장 메서드를 사용 하 여 IEnumerable을 배열로 변환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="a45a8-119">예제 3: 특정 기간 동안 쿼리를 사용 하 여 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="a45a8-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="a45a8-120">이 쿼리의 결과는 지난 24 시간으로 제한 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="a45a8-121">예제 4: 쿼리 결과에 렌더링 & 통계 포함</span><span class="sxs-lookup"><span data-stu-id="a45a8-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="a45a8-122">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)렌더링 및 통계 정보에 대 한 자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a45a8-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="a45a8-123">변수</span><span class="sxs-lookup"><span data-stu-id="a45a8-123">PARAMETERS</span></span>

### <span data-ttu-id="a45a8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a45a8-124">-AsJob</span></span>
<span data-ttu-id="a45a8-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a45a8-125">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45a8-126">-DefaultProfile</span></span>
<span data-ttu-id="a45a8-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="a45a8-128">-IncludeRender</span></span>
<span data-ttu-id="a45a8-129">지정 된 경우 메트릭 쿼리에 대 한 렌더링 정보가 응답에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-129">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="a45a8-130">-IncludeStatistics</span></span>
<span data-ttu-id="a45a8-131">지정 된 경우 쿼리 통계가 응답에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-131">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-132">-쿼리</span><span class="sxs-lookup"><span data-stu-id="a45a8-132">-Query</span></span>
<span data-ttu-id="a45a8-133">실행할 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-133">The query to execute.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-134">-Timespan</span><span class="sxs-lookup"><span data-stu-id="a45a8-134">-Timespan</span></span>
<span data-ttu-id="a45a8-135">쿼리를 바인딩할 timespan입니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-135">The timespan to bound the query by.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-136">-대기</span><span class="sxs-lookup"><span data-stu-id="a45a8-136">-Wait</span></span>
<span data-ttu-id="a45a8-137">서버가 쿼리를 처리 하는 데 소요 되는 시간에 상한을 배치 합니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="a45a8-138">보기 https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="a45a8-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-139">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="a45a8-139">-Workspace</span></span>
<span data-ttu-id="a45a8-140">작업 영역</span><span class="sxs-lookup"><span data-stu-id="a45a8-140">The workspace</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a45a8-141">-WorkspaceId</span></span>
<span data-ttu-id="a45a8-142">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-142">The workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45a8-143">CommonParameters</span></span>
<span data-ttu-id="a45a8-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45a8-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a45a8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45a8-146">입력</span><span class="sxs-lookup"><span data-stu-id="a45a8-146">INPUTS</span></span>

### <span data-ttu-id="a45a8-147">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="a45a8-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="a45a8-148">에서 파이프로 시작 되 면 작업 영역 ID가 PSWorkspace에서 추출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-148">If piped in, the workspace ID will be extracted from the PSWorkspace.</span></span> <span data-ttu-id="a45a8-149">그렇지 않으면 workspaceId 매개 변수를 사용 하 여 작업 영역 ID를 수동으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-149">Otherwise you can use the workspaceId parameter to specify the workspace ID manually.</span></span>

## <span data-ttu-id="a45a8-150">출력</span><span class="sxs-lookup"><span data-stu-id="a45a8-150">OUTPUTS</span></span>

### <span data-ttu-id="a45a8-151">OperationalInsights Queryresponse에 대 한 응답</span><span class="sxs-lookup"><span data-stu-id="a45a8-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>
<span data-ttu-id="a45a8-152">***Psqueryresponse*** 에는 쿼리의 결과, 렌더링 & 통계가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a45a8-152">The ***PSQueryResponse*** contains the Results, Render & Statistics of the query.</span></span>

## <span data-ttu-id="a45a8-153">상속자</span><span class="sxs-lookup"><span data-stu-id="a45a8-153">NOTES</span></span>

## <span data-ttu-id="a45a8-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a45a8-154">RELATED LINKS</span></span>

