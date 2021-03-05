---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: ce554f3591f022bdbc375c12a50ea9dae85b8baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998811"
---
# <span data-ttu-id="5ae60-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5ae60-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="5ae60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ae60-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae60-103">새 CosmosDB IndexingPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="5ae60-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ae60-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ae60-105">설명</span><span class="sxs-lookup"><span data-stu-id="5ae60-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae60-106">**New-AzCosmosDBGremlinIndexingPolicy** cmdlet은 PSIndexingPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="5ae60-107">예제</span><span class="sxs-lookup"><span data-stu-id="5ae60-107">EXAMPLES</span></span>

### <span data-ttu-id="5ae60-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ae60-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="5ae60-109">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="5ae60-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5ae60-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5ae60-110">PARAMETERS</span></span>

### <span data-ttu-id="5ae60-111">-자동</span><span class="sxs-lookup"><span data-stu-id="5ae60-111">-Automatic</span></span>
<span data-ttu-id="5ae60-112">인덱싱 정책이 자동인 경우를 나타내는 Bool</span><span class="sxs-lookup"><span data-stu-id="5ae60-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="5ae60-113">-CompositePath</span></span>
<span data-ttu-id="5ae60-114">Microsoft.Azure.Commands.CosmosDB.PSCompositePath 형식의 개체 배열</span><span class="sxs-lookup"><span data-stu-id="5ae60-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae60-115">-DefaultProfile</span></span>
<span data-ttu-id="5ae60-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-117">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="5ae60-117">-ExcludedPath</span></span>
<span data-ttu-id="5ae60-118">excludedPath를 포함하는 문자열 배열(Azure Cosmos DB 서비스에서 제외할 JSON 문서 내의 경로를 지정합니다.)  요소입니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-119">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="5ae60-119">-IncludedPath</span></span>
<span data-ttu-id="5ae60-120">includedPath를 포함하는 문자열 배열(Azure Cosmos DB 서비스에 포함될 JSON 문서 내의 경로를 지정합니다.) 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-121">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="5ae60-121">-IndexingMode</span></span>
<span data-ttu-id="5ae60-122">인덱싱 모드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="5ae60-123">가능한 값은 다음과 같습니다. '일관', 'Lazy', 'None'</span><span class="sxs-lookup"><span data-stu-id="5ae60-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="5ae60-124">-SpatialSpec</span></span>
<span data-ttu-id="5ae60-125">Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec 형식의 개체 배열</span><span class="sxs-lookup"><span data-stu-id="5ae60-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae60-126">CommonParameters</span></span>
<span data-ttu-id="5ae60-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ae60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae60-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ae60-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae60-129">입력</span><span class="sxs-lookup"><span data-stu-id="5ae60-129">INPUTS</span></span>

### <span data-ttu-id="5ae60-130">없음</span><span class="sxs-lookup"><span data-stu-id="5ae60-130">None</span></span>

## <span data-ttu-id="5ae60-131">출력</span><span class="sxs-lookup"><span data-stu-id="5ae60-131">OUTPUTS</span></span>

### <span data-ttu-id="5ae60-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="5ae60-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="5ae60-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ae60-133">NOTES</span></span>

## <span data-ttu-id="5ae60-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ae60-134">RELATED LINKS</span></span>
