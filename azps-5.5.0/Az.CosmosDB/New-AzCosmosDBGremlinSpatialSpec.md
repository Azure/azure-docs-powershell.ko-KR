---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinSpatialSpec.md
ms.openlocfilehash: 6cdb0d9732c64f26e2ba840623ae6f6df06602b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181316"
---
# <span data-ttu-id="df337-101">New-AzCosmosDBGremlinSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="df337-101">New-AzCosmosDBGremlinSpatialSpec</span></span>

## <span data-ttu-id="df337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df337-102">SYNOPSIS</span></span>
<span data-ttu-id="df337-103">PSSpatialSpec 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df337-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="df337-104">Set-AzCosmosDBGremlinIndexingPolicy에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df337-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIndexingPolicy.</span></span>

## <span data-ttu-id="df337-105">구문</span><span class="sxs-lookup"><span data-stu-id="df337-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df337-106">설명</span><span class="sxs-lookup"><span data-stu-id="df337-106">DESCRIPTION</span></span>
<span data-ttu-id="df337-107">Gremlin API의 SpatialSpec에 해당하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df337-107">Creates Object corresponding to Gremlin API's SpatialSpec.</span></span>

## <span data-ttu-id="df337-108">예제</span><span class="sxs-lookup"><span data-stu-id="df337-108">EXAMPLES</span></span>

### <span data-ttu-id="df337-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="df337-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="df337-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df337-110">PARAMETERS</span></span>

### <span data-ttu-id="df337-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df337-111">-DefaultProfile</span></span>
<span data-ttu-id="df337-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df337-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df337-113">-Path</span><span class="sxs-lookup"><span data-stu-id="df337-113">-Path</span></span>
<span data-ttu-id="df337-114">인덱싱할 JSON 문서의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="df337-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="df337-115">-Type</span><span class="sxs-lookup"><span data-stu-id="df337-115">-Type</span></span>
<span data-ttu-id="df337-116">허용 가능한 값이 있는 문자열 배열: Point, LineString, Polygon, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="df337-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="df337-117">공간 유형을 나타내는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="df337-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="df337-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df337-118">CommonParameters</span></span>
<span data-ttu-id="df337-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df337-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df337-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df337-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df337-121">입력</span><span class="sxs-lookup"><span data-stu-id="df337-121">INPUTS</span></span>

### <span data-ttu-id="df337-122">없음</span><span class="sxs-lookup"><span data-stu-id="df337-122">None</span></span>

## <span data-ttu-id="df337-123">출력</span><span class="sxs-lookup"><span data-stu-id="df337-123">OUTPUTS</span></span>

### <span data-ttu-id="df337-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="df337-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="df337-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df337-125">NOTES</span></span>

## <span data-ttu-id="df337-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df337-126">RELATED LINKS</span></span>
