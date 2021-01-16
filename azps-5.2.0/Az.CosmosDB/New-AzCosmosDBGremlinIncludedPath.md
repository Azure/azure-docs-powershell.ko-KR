---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348981"
---
# <span data-ttu-id="06f24-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="06f24-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="06f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f24-102">SYNOPSIS</span></span>
<span data-ttu-id="06f24-103">PSIncludedPath 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="06f24-104">Set-AzCosmosDBGremlinGraph에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="06f24-105">구문</span><span class="sxs-lookup"><span data-stu-id="06f24-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06f24-106">설명</span><span class="sxs-lookup"><span data-stu-id="06f24-106">DESCRIPTION</span></span>
<span data-ttu-id="06f24-107">Gremlin API의 IncludedPath에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="06f24-108">예제</span><span class="sxs-lookup"><span data-stu-id="06f24-108">EXAMPLES</span></span>

### <span data-ttu-id="06f24-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="06f24-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="06f24-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06f24-110">PARAMETERS</span></span>

### <span data-ttu-id="06f24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f24-111">-DefaultProfile</span></span>
<span data-ttu-id="06f24-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06f24-113">-Index</span><span class="sxs-lookup"><span data-stu-id="06f24-113">-Index</span></span>
<span data-ttu-id="06f24-114">이 경로에 대한 인덱스 목록</span><span class="sxs-lookup"><span data-stu-id="06f24-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f24-115">-Path</span><span class="sxs-lookup"><span data-stu-id="06f24-115">-Path</span></span>
<span data-ttu-id="06f24-116">인덱싱 동작이 적용되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="06f24-117">인덱스 경로는 일반적으로 루트로 시작하고 와일드카드(/path/\*)로 끝날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="06f24-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f24-118">CommonParameters</span></span>
<span data-ttu-id="06f24-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06f24-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f24-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06f24-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f24-121">입력</span><span class="sxs-lookup"><span data-stu-id="06f24-121">INPUTS</span></span>

### <span data-ttu-id="06f24-122">없음</span><span class="sxs-lookup"><span data-stu-id="06f24-122">None</span></span>

## <span data-ttu-id="06f24-123">출력</span><span class="sxs-lookup"><span data-stu-id="06f24-123">OUTPUTS</span></span>

### <span data-ttu-id="06f24-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="06f24-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="06f24-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06f24-125">NOTES</span></span>

## <span data-ttu-id="06f24-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06f24-126">RELATED LINKS</span></span>