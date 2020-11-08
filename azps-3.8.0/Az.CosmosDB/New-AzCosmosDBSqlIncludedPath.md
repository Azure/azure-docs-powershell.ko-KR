---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043641"
---
# <span data-ttu-id="c040b-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="c040b-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="c040b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c040b-102">SYNOPSIS</span></span>
<span data-ttu-id="c040b-103">PSIncludedPath 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="c040b-104">Set-AzCosmosDBSqlContainer에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="c040b-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c040b-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c040b-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c040b-106">DESCRIPTION</span></span>
<span data-ttu-id="c040b-107">Sql API의 IncludedPath에 해당 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="c040b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c040b-108">EXAMPLES</span></span>

### <span data-ttu-id="c040b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c040b-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="c040b-110">변수</span><span class="sxs-lookup"><span data-stu-id="c040b-110">PARAMETERS</span></span>

### <span data-ttu-id="c040b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c040b-111">-DefaultProfile</span></span>
<span data-ttu-id="c040b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c040b-113">-인덱스</span><span class="sxs-lookup"><span data-stu-id="c040b-113">-Index</span></span>
<span data-ttu-id="c040b-114">이 경로의 인덱스 목록</span><span class="sxs-lookup"><span data-stu-id="c040b-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="c040b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c040b-115">-Path</span></span>
<span data-ttu-id="c040b-116">인덱싱 동작이 적용 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="c040b-117">일반적으로 인덱스 경로는 와일드 카드 (/path/\*)를 사용 하 여 root로 시작 하 고 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="c040b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c040b-118">CommonParameters</span></span>
<span data-ttu-id="c040b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c040b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c040b-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c040b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c040b-121">입력</span><span class="sxs-lookup"><span data-stu-id="c040b-121">INPUTS</span></span>

### <span data-ttu-id="c040b-122">않아야</span><span class="sxs-lookup"><span data-stu-id="c040b-122">None</span></span>

## <span data-ttu-id="c040b-123">출력</span><span class="sxs-lookup"><span data-stu-id="c040b-123">OUTPUTS</span></span>

### <span data-ttu-id="c040b-124">CosmosDB. PSIncludedPath/.</span><span class="sxs-lookup"><span data-stu-id="c040b-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="c040b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="c040b-125">NOTES</span></span>

## <span data-ttu-id="c040b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c040b-126">RELATED LINKS</span></span>
