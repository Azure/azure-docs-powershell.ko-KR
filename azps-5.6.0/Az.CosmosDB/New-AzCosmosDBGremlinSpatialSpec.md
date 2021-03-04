---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 8285afa9ba3764058f12ef0d8bfae009735a5ca3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957451"
---
# <span data-ttu-id="3a834-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="3a834-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="3a834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a834-102">SYNOPSIS</span></span>
<span data-ttu-id="3a834-103">PSSpatialSpec 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="3a834-104">Set-AzCosmosDBGremlinIndexingPolicy의 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="3a834-105">구문</span><span class="sxs-lookup"><span data-stu-id="3a834-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a834-106">설명</span><span class="sxs-lookup"><span data-stu-id="3a834-106">DESCRIPTION</span></span>
<span data-ttu-id="3a834-107">Gremlin API의 SpatialSpec에 해당하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="3a834-108">예제</span><span class="sxs-lookup"><span data-stu-id="3a834-108">EXAMPLES</span></span>

### <span data-ttu-id="3a834-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a834-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="3a834-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3a834-110">PARAMETERS</span></span>

### <span data-ttu-id="3a834-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a834-111">-DefaultProfile</span></span>
<span data-ttu-id="3a834-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a834-113">-Path</span><span class="sxs-lookup"><span data-stu-id="3a834-113">-Path</span></span>
<span data-ttu-id="3a834-114">인덱싱할 JSON 문서의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="3a834-115">-Type</span><span class="sxs-lookup"><span data-stu-id="3a834-115">-Type</span></span>
<span data-ttu-id="3a834-116">허용 가능한 값이 있는 문자열 배열: 점, LineString, Polygon, MultiPolygon입니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="3a834-117">공간 형식을 나타내는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-117">Represent's paths spatial type.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a834-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a834-118">CommonParameters</span></span>
<span data-ttu-id="3a834-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a834-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a834-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a834-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a834-121">입력</span><span class="sxs-lookup"><span data-stu-id="3a834-121">INPUTS</span></span>

### <span data-ttu-id="3a834-122">없음</span><span class="sxs-lookup"><span data-stu-id="3a834-122">None</span></span>

## <span data-ttu-id="3a834-123">출력</span><span class="sxs-lookup"><span data-stu-id="3a834-123">OUTPUTS</span></span>

### <span data-ttu-id="3a834-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="3a834-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="3a834-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a834-125">NOTES</span></span>

## <span data-ttu-id="3a834-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a834-126">RELATED LINKS</span></span>
