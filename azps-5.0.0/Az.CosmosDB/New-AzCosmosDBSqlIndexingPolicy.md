---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306989"
---
# <span data-ttu-id="0bb3f-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0bb3f-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="0bb3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb3f-103">새 CosmosDB Sql IndexingPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="0bb3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0bb3f-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bb3f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0bb3f-105">DESCRIPTION</span></span>
<span data-ttu-id="0bb3f-106">**AzCosmosDBSqlIndexingPolicy** Cmdlet은 PSSqlIndexingPolicy 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="0bb3f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0bb3f-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb3f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0bb3f-108">Example 1</span></span>
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

## <span data-ttu-id="0bb3f-109">변수</span><span class="sxs-lookup"><span data-stu-id="0bb3f-109">PARAMETERS</span></span>

### <span data-ttu-id="0bb3f-110">-자동</span><span class="sxs-lookup"><span data-stu-id="0bb3f-110">-Automatic</span></span>
<span data-ttu-id="0bb3f-111">인덱싱 정책이 자동 인지 여부를 나타내는 부울</span><span class="sxs-lookup"><span data-stu-id="0bb3f-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="0bb3f-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="0bb3f-112">-CompositePath</span></span>
<span data-ttu-id="0bb3f-113">CosmosDB. PSCompositePath에 해당 하는 개체 배열의 배열 형식</span><span class="sxs-lookup"><span data-stu-id="0bb3f-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="0bb3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb3f-114">-DefaultProfile</span></span>
<span data-ttu-id="0bb3f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bb3f-116">-ExcludedPath</span><span class="sxs-lookup"><span data-stu-id="0bb3f-116">-ExcludedPath</span></span>
<span data-ttu-id="0bb3f-117">ExcludedPath를 포함 하는 문자열 배열 (Azure Cosmos DB 서비스에서 제외할 JSON 문서 내의 경로를 지정 합니다.)  요소.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="0bb3f-118">-IncludedPath</span><span class="sxs-lookup"><span data-stu-id="0bb3f-118">-IncludedPath</span></span>
<span data-ttu-id="0bb3f-119">IncludedPath를 포함 하는 문자열 배열 (Azure Cosmos DB service에 포함할 JSON 문서 내의 경로를 지정 합니다.) 요소.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="0bb3f-120">-IndexingMode</span><span class="sxs-lookup"><span data-stu-id="0bb3f-120">-IndexingMode</span></span>
<span data-ttu-id="0bb3f-121">인덱싱 모드를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-121">indicates the indexing mode.</span></span>
<span data-ttu-id="0bb3f-122">사용할 수 있는 값은 다음과 같습니다. ' 일관성 ', ' 지연 ', ' 없음 '</span><span class="sxs-lookup"><span data-stu-id="0bb3f-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="0bb3f-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="0bb3f-123">-SpatialSpec</span></span>
<span data-ttu-id="0bb3f-124">CosmosDB. PSSpatialSpec에 해당 하는 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="0bb3f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb3f-125">CommonParameters</span></span>
<span data-ttu-id="0bb3f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb3f-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0bb3f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb3f-128">입력</span><span class="sxs-lookup"><span data-stu-id="0bb3f-128">INPUTS</span></span>

### <span data-ttu-id="0bb3f-129">않아야</span><span class="sxs-lookup"><span data-stu-id="0bb3f-129">None</span></span>

## <span data-ttu-id="0bb3f-130">출력</span><span class="sxs-lookup"><span data-stu-id="0bb3f-130">OUTPUTS</span></span>

### <span data-ttu-id="0bb3f-131">CosmosDB. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0bb3f-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="0bb3f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0bb3f-132">NOTES</span></span>

## <span data-ttu-id="0bb3f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bb3f-133">RELATED LINKS</span></span>
