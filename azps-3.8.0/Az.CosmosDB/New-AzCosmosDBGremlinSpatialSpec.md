---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043648"
---
# <span data-ttu-id="86ba3-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="86ba3-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="86ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="86ba3-103">PSSpatialSpec 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="86ba3-104">Set-AzCosmosDBGremlinIndexingPolicy에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="86ba3-105">구문과</span><span class="sxs-lookup"><span data-stu-id="86ba3-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86ba3-106">설명은</span><span class="sxs-lookup"><span data-stu-id="86ba3-106">DESCRIPTION</span></span>
<span data-ttu-id="86ba3-107">Gremlin API의 SpatialSpec에 해당 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="86ba3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="86ba3-108">EXAMPLES</span></span>

### <span data-ttu-id="86ba3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="86ba3-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="86ba3-110">변수</span><span class="sxs-lookup"><span data-stu-id="86ba3-110">PARAMETERS</span></span>

### <span data-ttu-id="86ba3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ba3-111">-DefaultProfile</span></span>
<span data-ttu-id="86ba3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86ba3-113">-Path</span><span class="sxs-lookup"><span data-stu-id="86ba3-113">-Path</span></span>
<span data-ttu-id="86ba3-114">Index에 대 한 JSON 문서의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="86ba3-115">-Type</span><span class="sxs-lookup"><span data-stu-id="86ba3-115">-Type</span></span>
<span data-ttu-id="86ba3-116">점, LineString, 다각형, 다중 다각형이 허용 되는 값을 갖는 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="86ba3-117">공간 형식의 경로를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="86ba3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ba3-118">CommonParameters</span></span>
<span data-ttu-id="86ba3-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86ba3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ba3-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86ba3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ba3-121">입력</span><span class="sxs-lookup"><span data-stu-id="86ba3-121">INPUTS</span></span>

### <span data-ttu-id="86ba3-122">않아야</span><span class="sxs-lookup"><span data-stu-id="86ba3-122">None</span></span>

## <span data-ttu-id="86ba3-123">출력</span><span class="sxs-lookup"><span data-stu-id="86ba3-123">OUTPUTS</span></span>

### <span data-ttu-id="86ba3-124">CosmosDB. PSSpatialSpec/.</span><span class="sxs-lookup"><span data-stu-id="86ba3-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="86ba3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="86ba3-125">NOTES</span></span>

## <span data-ttu-id="86ba3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86ba3-126">RELATED LINKS</span></span>
