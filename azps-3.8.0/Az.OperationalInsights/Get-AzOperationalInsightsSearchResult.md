---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 254402902fe1e4a3d1ac4e683094731472929f87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042039"
---
# <span data-ttu-id="60bae-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="60bae-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="60bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60bae-102">SYNOPSIS</span></span>
<span data-ttu-id="60bae-103">지정 된 매개 변수를 기준으로 검색 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="60bae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60bae-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60bae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60bae-105">DESCRIPTION</span></span>
<span data-ttu-id="60bae-106">**AzOperationalInsightsSearchResult** cmdlet은 지정 된 매개 변수를 기준으로 검색 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="60bae-107">반환 된 개체의 Metadata 속성에서 검색 상태에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="60bae-108">상태가 보류 중 이면 검색이 완료 되지 않은 것 이며 결과는 보관 파일에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="60bae-109">반환 된 개체의 Value 속성에서 검색 결과를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="60bae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="60bae-110">EXAMPLES</span></span>

### <span data-ttu-id="60bae-111">예제 1: 쿼리를 사용 하 여 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="60bae-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="60bae-112">이 명령은 쿼리를 사용 하 여 모든 검색 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="60bae-113">예제 2: ID를 사용 하 여 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="60bae-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="60bae-114">이 명령은 ID를 사용 하 여 검색 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="60bae-115">예제 3: 검색을 완료 한 후 결과 표시</span><span class="sxs-lookup"><span data-stu-id="60bae-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="60bae-116">이 스크립트는 검색을 시작 하 고 결과를 표시 하기 전에 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="60bae-117">변수</span><span class="sxs-lookup"><span data-stu-id="60bae-117">PARAMETERS</span></span>

### <span data-ttu-id="60bae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bae-118">-DefaultProfile</span></span>
<span data-ttu-id="60bae-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60bae-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60bae-120">엔드</span><span class="sxs-lookup"><span data-stu-id="60bae-120">-End</span></span>
<span data-ttu-id="60bae-121">쿼리 된 시간 범위의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-122">-Id</span><span class="sxs-lookup"><span data-stu-id="60bae-122">-Id</span></span>
<span data-ttu-id="60bae-123">Id를 지정 하면 해당 id에 대 한 검색 결과가 원본 쿼리 매개 변수를 사용 하 여 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="60bae-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-125">-사전 강조 표시</span><span class="sxs-lookup"><span data-stu-id="60bae-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-126">-쿼리</span><span class="sxs-lookup"><span data-stu-id="60bae-126">-Query</span></span>
<span data-ttu-id="60bae-127">실행할 검색 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60bae-128">-ResourceGroupName</span></span>
<span data-ttu-id="60bae-129">작업 영역을 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-130">-시작</span><span class="sxs-lookup"><span data-stu-id="60bae-130">-Start</span></span>
<span data-ttu-id="60bae-131">쿼리 된 시간 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="60bae-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-132">-위쪽</span><span class="sxs-lookup"><span data-stu-id="60bae-132">-Top</span></span>
<span data-ttu-id="60bae-133">반환 될 최대 결과 수 (5000으로 제한 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="60bae-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="60bae-134">-WorkspaceName</span></span>
<span data-ttu-id="60bae-135">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60bae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bae-136">CommonParameters</span></span>
<span data-ttu-id="60bae-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60bae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bae-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60bae-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bae-139">입력</span><span class="sxs-lookup"><span data-stu-id="60bae-139">INPUTS</span></span>

### <span data-ttu-id="60bae-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60bae-140">System.String</span></span>

### <span data-ttu-id="60bae-141">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="60bae-141">System.Int64</span></span>

### <span data-ttu-id="60bae-142">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60bae-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="60bae-143">출력</span><span class="sxs-lookup"><span data-stu-id="60bae-143">OUTPUTS</span></span>

### <span data-ttu-id="60bae-144">OperationalInsights. PSSearchGetSearchResultsResponse/.</span><span class="sxs-lookup"><span data-stu-id="60bae-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="60bae-145">상속자</span><span class="sxs-lookup"><span data-stu-id="60bae-145">NOTES</span></span>

## <span data-ttu-id="60bae-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60bae-146">RELATED LINKS</span></span>

[<span data-ttu-id="60bae-147">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="60bae-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)


