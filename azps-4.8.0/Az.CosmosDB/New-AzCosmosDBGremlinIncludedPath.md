---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPath.md
ms.openlocfilehash: 779589d3789e9b6baa1864f22366fb40b1c41c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056460"
---
# <span data-ttu-id="e7252-101">New-AzCosmosDBGremlinIncludedPath</span><span class="sxs-lookup"><span data-stu-id="e7252-101">New-AzCosmosDBGremlinIncludedPath</span></span>

## <span data-ttu-id="e7252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7252-102">SYNOPSIS</span></span>
<span data-ttu-id="e7252-103">PSIncludedPath 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="e7252-104">Set-AzCosmosDBGremlinGraph에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="e7252-105">구문과</span><span class="sxs-lookup"><span data-stu-id="e7252-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7252-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e7252-106">DESCRIPTION</span></span>
<span data-ttu-id="e7252-107">Gremlin API의 IncludedPath에 해당 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-107">Object corresponding to Gremlin API's IncludedPath.</span></span>

## <span data-ttu-id="e7252-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e7252-108">EXAMPLES</span></span>

### <span data-ttu-id="e7252-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7252-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $index1
Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="e7252-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7252-110">PARAMETERS</span></span>

### <span data-ttu-id="e7252-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7252-111">-DefaultProfile</span></span>
<span data-ttu-id="e7252-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7252-113">-인덱스</span><span class="sxs-lookup"><span data-stu-id="e7252-113">-Index</span></span>
<span data-ttu-id="e7252-114">이 경로의 인덱스 목록</span><span class="sxs-lookup"><span data-stu-id="e7252-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="e7252-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e7252-115">-Path</span></span>
<span data-ttu-id="e7252-116">인덱싱 동작이 적용 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="e7252-117">일반적으로 인덱스 경로는 와일드 카드 (/path/\*)를 사용 하 여 root로 시작 하 고 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="e7252-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7252-118">CommonParameters</span></span>
<span data-ttu-id="e7252-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7252-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7252-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7252-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7252-121">입력</span><span class="sxs-lookup"><span data-stu-id="e7252-121">INPUTS</span></span>

### <span data-ttu-id="e7252-122">않아야</span><span class="sxs-lookup"><span data-stu-id="e7252-122">None</span></span>

## <span data-ttu-id="e7252-123">출력</span><span class="sxs-lookup"><span data-stu-id="e7252-123">OUTPUTS</span></span>

### <span data-ttu-id="e7252-124">CosmosDB. PSIncludedPath/.</span><span class="sxs-lookup"><span data-stu-id="e7252-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="e7252-125">상속자</span><span class="sxs-lookup"><span data-stu-id="e7252-125">NOTES</span></span>

## <span data-ttu-id="e7252-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7252-126">RELATED LINKS</span></span>
