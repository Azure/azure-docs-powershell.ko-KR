---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365156"
---
# <span data-ttu-id="4d171-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="4d171-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="4d171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d171-102">SYNOPSIS</span></span>
<span data-ttu-id="4d171-103">PSSpatialSpec 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="4d171-104">Set-AzCosmosDBSqlIndexingPolicy에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="4d171-105">구문</span><span class="sxs-lookup"><span data-stu-id="4d171-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d171-106">설명</span><span class="sxs-lookup"><span data-stu-id="4d171-106">DESCRIPTION</span></span>
<span data-ttu-id="4d171-107">Sql API의 SpatialSpec에 해당하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="4d171-108">예제</span><span class="sxs-lookup"><span data-stu-id="4d171-108">EXAMPLES</span></span>

### <span data-ttu-id="4d171-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d171-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="4d171-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d171-110">PARAMETERS</span></span>

### <span data-ttu-id="4d171-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d171-111">-DefaultProfile</span></span>
<span data-ttu-id="4d171-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d171-113">-Path</span><span class="sxs-lookup"><span data-stu-id="4d171-113">-Path</span></span>
<span data-ttu-id="4d171-114">인덱싱할 JSON 문서의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="4d171-115">-Type</span><span class="sxs-lookup"><span data-stu-id="4d171-115">-Type</span></span>
<span data-ttu-id="4d171-116">허용 가능한 값이 있는 문자열 배열: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="4d171-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="4d171-117">공간 유형을 나타내는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="4d171-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d171-118">CommonParameters</span></span>
<span data-ttu-id="4d171-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d171-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d171-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d171-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d171-121">입력</span><span class="sxs-lookup"><span data-stu-id="4d171-121">INPUTS</span></span>

### <span data-ttu-id="4d171-122">없음</span><span class="sxs-lookup"><span data-stu-id="4d171-122">None</span></span>

## <span data-ttu-id="4d171-123">출력</span><span class="sxs-lookup"><span data-stu-id="4d171-123">OUTPUTS</span></span>

### <span data-ttu-id="4d171-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="4d171-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="4d171-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d171-125">NOTES</span></span>

## <span data-ttu-id="4d171-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d171-126">RELATED LINKS</span></span>
