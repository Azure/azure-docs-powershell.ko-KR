---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: a9d77cc76521eca1e99dac630673ef3825d1155b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962432"
---
# <span data-ttu-id="27eaf-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="27eaf-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="27eaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="27eaf-103">PSIncludedPath 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="27eaf-104">Set-AzCosmosDBSqlContainer의 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="27eaf-105">구문</span><span class="sxs-lookup"><span data-stu-id="27eaf-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27eaf-106">설명</span><span class="sxs-lookup"><span data-stu-id="27eaf-106">DESCRIPTION</span></span>
<span data-ttu-id="27eaf-107">Sql API의 IncludedPath에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="27eaf-108">예제</span><span class="sxs-lookup"><span data-stu-id="27eaf-108">EXAMPLES</span></span>

### <span data-ttu-id="27eaf-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="27eaf-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="27eaf-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27eaf-110">PARAMETERS</span></span>

### <span data-ttu-id="27eaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27eaf-111">-DefaultProfile</span></span>
<span data-ttu-id="27eaf-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27eaf-113">-Index</span><span class="sxs-lookup"><span data-stu-id="27eaf-113">-Index</span></span>
<span data-ttu-id="27eaf-114">이 경로에 대한 인덱스 목록</span><span class="sxs-lookup"><span data-stu-id="27eaf-114">List of indexes for this path</span></span>

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

### <span data-ttu-id="27eaf-115">-Path</span><span class="sxs-lookup"><span data-stu-id="27eaf-115">-Path</span></span>
<span data-ttu-id="27eaf-116">인덱싱 동작이 적용되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="27eaf-117">인덱스 경로는 일반적으로 루트로 시작하고 와일드카드(/path/\*)로 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="27eaf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27eaf-118">CommonParameters</span></span>
<span data-ttu-id="27eaf-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27eaf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27eaf-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27eaf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27eaf-121">입력</span><span class="sxs-lookup"><span data-stu-id="27eaf-121">INPUTS</span></span>

### <span data-ttu-id="27eaf-122">없음</span><span class="sxs-lookup"><span data-stu-id="27eaf-122">None</span></span>

## <span data-ttu-id="27eaf-123">출력</span><span class="sxs-lookup"><span data-stu-id="27eaf-123">OUTPUTS</span></span>

### <span data-ttu-id="27eaf-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="27eaf-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="27eaf-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27eaf-125">NOTES</span></span>

## <span data-ttu-id="27eaf-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27eaf-126">RELATED LINKS</span></span>
