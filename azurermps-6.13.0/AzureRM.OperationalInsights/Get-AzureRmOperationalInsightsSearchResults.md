---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSearchResults.md
ms.openlocfilehash: 547988d2079f35b82af3638e3e4f09b101d8fbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524343"
---
# <span data-ttu-id="fe943-101">Get-AzureRmOperationalInsightsSearchResults</span><span class="sxs-lookup"><span data-stu-id="fe943-101">Get-AzureRmOperationalInsightsSearchResults</span></span>

## <span data-ttu-id="fe943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe943-102">SYNOPSIS</span></span>
<span data-ttu-id="fe943-103">지정 된 매개 변수를 기준으로 검색 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe943-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe943-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Top] <Int64>] [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>]
 [[-Start] <DateTime>] [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe943-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe943-105">DESCRIPTION</span></span>
<span data-ttu-id="fe943-106">**AzureRmOperationalInsightsSearchResults** cmdlet은 지정 된 매개 변수를 기준으로 검색 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-106">The **Get-AzureRmOperationalInsightsSearchResults** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="fe943-107">반환 된 개체의 Metadata 속성에서 검색 상태에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="fe943-108">상태가 보류 중 이면 검색이 완료 되지 않은 것 이며 결과는 보관 파일에서 가져온 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="fe943-109">반환 된 개체의 Value 속성에서 검색 결과를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="fe943-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fe943-110">EXAMPLES</span></span>

### <span data-ttu-id="fe943-111">예제 1: 쿼리를 사용 하 여 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe943-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="fe943-112">이 명령은 쿼리를 사용 하 여 모든 검색 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="fe943-113">예제 2: ID를 사용 하 여 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe943-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="fe943-114">이 명령은 ID를 사용 하 여 검색 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="fe943-115">예제 3: 검색을 완료 한 후 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fe943-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzureRmOperationalInsightsSearchResults -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="fe943-116">이 스크립트는 검색을 시작 하 고 결과를 표시 하기 전에 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="fe943-117">변수</span><span class="sxs-lookup"><span data-stu-id="fe943-117">PARAMETERS</span></span>

### <span data-ttu-id="fe943-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe943-118">-DefaultProfile</span></span>
<span data-ttu-id="fe943-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fe943-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe943-120">엔드</span><span class="sxs-lookup"><span data-stu-id="fe943-120">-End</span></span>
<span data-ttu-id="fe943-121">쿼리 된 시간 범위의 끝입니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-121">End of the queried time range.</span></span>

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

### <span data-ttu-id="fe943-122">-Id</span><span class="sxs-lookup"><span data-stu-id="fe943-122">-Id</span></span>
<span data-ttu-id="fe943-123">Id를 지정 하면 해당 id에 대 한 검색 결과가 원본 쿼리 매개 변수를 사용 하 여 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

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

### <span data-ttu-id="fe943-124">-PostHighlight</span><span class="sxs-lookup"><span data-stu-id="fe943-124">-PostHighlight</span></span>
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

### <span data-ttu-id="fe943-125">-사전 강조 표시</span><span class="sxs-lookup"><span data-stu-id="fe943-125">-PreHighlight</span></span>
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

### <span data-ttu-id="fe943-126">-쿼리</span><span class="sxs-lookup"><span data-stu-id="fe943-126">-Query</span></span>
<span data-ttu-id="fe943-127">실행할 검색 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-127">The search query that will be executed.</span></span>

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

### <span data-ttu-id="fe943-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe943-128">-ResourceGroupName</span></span>
<span data-ttu-id="fe943-129">작업 영역을 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-129">The name of the resource group that contains the workspace.</span></span>

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

### <span data-ttu-id="fe943-130">-시작</span><span class="sxs-lookup"><span data-stu-id="fe943-130">-Start</span></span>
<span data-ttu-id="fe943-131">쿼리 된 시간 범위의 시작</span><span class="sxs-lookup"><span data-stu-id="fe943-131">Start of the queried time range.</span></span>

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

### <span data-ttu-id="fe943-132">-위쪽</span><span class="sxs-lookup"><span data-stu-id="fe943-132">-Top</span></span>
<span data-ttu-id="fe943-133">반환 될 최대 결과 수 (5000으로 제한 됩니다.)</span><span class="sxs-lookup"><span data-stu-id="fe943-133">The maximum number of results to be returned, limited to 5000.</span></span>

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

### <span data-ttu-id="fe943-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe943-134">-WorkspaceName</span></span>
<span data-ttu-id="fe943-135">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-135">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="fe943-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe943-136">CommonParameters</span></span>
<span data-ttu-id="fe943-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe943-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe943-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe943-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe943-139">입력</span><span class="sxs-lookup"><span data-stu-id="fe943-139">INPUTS</span></span>

### <span data-ttu-id="fe943-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fe943-140">System.String</span></span>

### <span data-ttu-id="fe943-141">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="fe943-141">System.Int64</span></span>

### <span data-ttu-id="fe943-142">시스템 Null 허용 ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fe943-142">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fe943-143">출력</span><span class="sxs-lookup"><span data-stu-id="fe943-143">OUTPUTS</span></span>

### <span data-ttu-id="fe943-144">OperationalInsights. PSSearchGetSearchResultsResponse/.</span><span class="sxs-lookup"><span data-stu-id="fe943-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="fe943-145">상속자</span><span class="sxs-lookup"><span data-stu-id="fe943-145">NOTES</span></span>

## <span data-ttu-id="fe943-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe943-146">RELATED LINKS</span></span>

[<span data-ttu-id="fe943-147">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="fe943-147">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>](./Get-AzureRmOperationalInsightsSavedSearchResults.md)


