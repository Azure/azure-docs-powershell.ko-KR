---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306980"
---
# <span data-ttu-id="9fd2a-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="9fd2a-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="9fd2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd2a-103">PSSpatialSpec 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="9fd2a-104">Set-AzCosmosDBSqlIndexingPolicy에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="9fd2a-105">구문과</span><span class="sxs-lookup"><span data-stu-id="9fd2a-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fd2a-106">설명은</span><span class="sxs-lookup"><span data-stu-id="9fd2a-106">DESCRIPTION</span></span>
<span data-ttu-id="9fd2a-107">Sql API의 SpatialSpec에 해당 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="9fd2a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9fd2a-108">EXAMPLES</span></span>

### <span data-ttu-id="9fd2a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fd2a-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="9fd2a-110">변수</span><span class="sxs-lookup"><span data-stu-id="9fd2a-110">PARAMETERS</span></span>

### <span data-ttu-id="9fd2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd2a-111">-DefaultProfile</span></span>
<span data-ttu-id="9fd2a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fd2a-113">-Path</span><span class="sxs-lookup"><span data-stu-id="9fd2a-113">-Path</span></span>
<span data-ttu-id="9fd2a-114">Index에 대 한 JSON 문서의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="9fd2a-115">-Type</span><span class="sxs-lookup"><span data-stu-id="9fd2a-115">-Type</span></span>
<span data-ttu-id="9fd2a-116">점, LineString, 다각형, 다중 다각형이 허용 되는 값을 갖는 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="9fd2a-117">공간 형식의 경로를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="9fd2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd2a-118">CommonParameters</span></span>
<span data-ttu-id="9fd2a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd2a-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd2a-121">입력</span><span class="sxs-lookup"><span data-stu-id="9fd2a-121">INPUTS</span></span>

### <span data-ttu-id="9fd2a-122">않아야</span><span class="sxs-lookup"><span data-stu-id="9fd2a-122">None</span></span>

## <span data-ttu-id="9fd2a-123">출력</span><span class="sxs-lookup"><span data-stu-id="9fd2a-123">OUTPUTS</span></span>

### <span data-ttu-id="9fd2a-124">CosmosDB. PSSpatialSpec/.</span><span class="sxs-lookup"><span data-stu-id="9fd2a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="9fd2a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="9fd2a-125">NOTES</span></span>

## <span data-ttu-id="9fd2a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fd2a-126">RELATED LINKS</span></span>
