---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493683"
---
# <span data-ttu-id="0c538-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0c538-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="0c538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c538-102">SYNOPSIS</span></span>
<span data-ttu-id="0c538-103">새 CosmosDB Sql IndexingPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="0c538-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c538-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c538-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c538-105">DESCRIPTION</span></span>
<span data-ttu-id="0c538-106">**New-AzCosmosDBSqlIndexingPolicy** cmdlet은 PSSqlIndexingPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="0c538-107">예제</span><span class="sxs-lookup"><span data-stu-id="0c538-107">EXAMPLES</span></span>

### <span data-ttu-id="0c538-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c538-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="0c538-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c538-109">PARAMETERS</span></span>

### <span data-ttu-id="0c538-110">-Automatic</span><span class="sxs-lookup"><span data-stu-id="0c538-110">-Automatic</span></span>
<span data-ttu-id="0c538-111">인덱싱 정책이 자동인 경우를 나타내는 Bool</span><span class="sxs-lookup"><span data-stu-id="0c538-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="0c538-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="0c538-112">-CompositePath</span></span>
<span data-ttu-id="0c538-113">Microsoft.Azure.Commands.CosmosDB.PSCompositePath 유형의 개체 배열</span><span class="sxs-lookup"><span data-stu-id="0c538-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="0c538-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c538-114">-DefaultProfile</span></span>
<span data-ttu-id="0c538-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c538-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="0c538-116">-ExcludedPath</span></span>
<span data-ttu-id="0c538-117">excludedPath를 포함하는 문자열 배열(Azure Cosmos DB 서비스에서 제외할 JSON 문서 내의 경로를 지정합니다.)  요소.</span><span class="sxs-lookup"><span data-stu-id="0c538-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="0c538-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="0c538-118">-IncludedPath</span></span>
<span data-ttu-id="0c538-119">includedPath(Azure Cosmos DB 서비스에 포함될 JSON 문서 내의 경로를 지정)를 포함하는 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="0c538-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="0c538-120">-IndexingMode</span></span>
<span data-ttu-id="0c538-121">인덱싱 모드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-121">indicates the indexing mode.</span></span>
<span data-ttu-id="0c538-122">가능한 값은 'Consistent', 'Lazy', 'None'입니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="0c538-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="0c538-123">-SpatialSpec</span></span>
<span data-ttu-id="0c538-124">Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec 유형의 개체 배열</span><span class="sxs-lookup"><span data-stu-id="0c538-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="0c538-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c538-125">CommonParameters</span></span>
<span data-ttu-id="0c538-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c538-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c538-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c538-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c538-128">입력</span><span class="sxs-lookup"><span data-stu-id="0c538-128">INPUTS</span></span>

### <span data-ttu-id="0c538-129">없음</span><span class="sxs-lookup"><span data-stu-id="0c538-129">None</span></span>

## <span data-ttu-id="0c538-130">출력</span><span class="sxs-lookup"><span data-stu-id="0c538-130">OUTPUTS</span></span>

### <span data-ttu-id="0c538-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0c538-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="0c538-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c538-132">NOTES</span></span>

## <span data-ttu-id="0c538-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c538-133">RELATED LINKS</span></span>
