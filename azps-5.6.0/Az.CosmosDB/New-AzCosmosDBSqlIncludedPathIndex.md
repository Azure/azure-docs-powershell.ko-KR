---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: c9a50c833de9290e08ac211b52586d25e5082c59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960848"
---
# <span data-ttu-id="92da4-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="92da4-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="92da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92da4-102">SYNOPSIS</span></span>
<span data-ttu-id="92da4-103">PSIndexes 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="92da4-104">Set-AzCosmosDBSqlIncludedPath에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="92da4-105">구문</span><span class="sxs-lookup"><span data-stu-id="92da4-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92da4-106">설명</span><span class="sxs-lookup"><span data-stu-id="92da4-106">DESCRIPTION</span></span>
<span data-ttu-id="92da4-107">Sql API의 IncludedPath의 인덱스에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="92da4-108">예제</span><span class="sxs-lookup"><span data-stu-id="92da4-108">EXAMPLES</span></span>

### <span data-ttu-id="92da4-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="92da4-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="92da4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="92da4-110">PARAMETERS</span></span>

### <span data-ttu-id="92da4-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="92da4-111">-DataType</span></span>
<span data-ttu-id="92da4-112">인덱싱 동작이 적용되는 데이터형입니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="92da4-113">가능한 값에는 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon' 등이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="92da4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92da4-114">-DefaultProfile</span></span>
<span data-ttu-id="92da4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92da4-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="92da4-116">-Kind</span></span>
<span data-ttu-id="92da4-117">인덱스 유형을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-117">Indicates the type of index.</span></span>
<span data-ttu-id="92da4-118">가능한 값에는 '해시', 'Range', 'Spatial'이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="92da4-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="92da4-119">-Precision</span></span>
<span data-ttu-id="92da4-120">인덱스의 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-120">The precision of the index.</span></span>
<span data-ttu-id="92da4-121">-1은 최대 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92da4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92da4-122">CommonParameters</span></span>
<span data-ttu-id="92da4-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92da4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92da4-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92da4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92da4-125">입력</span><span class="sxs-lookup"><span data-stu-id="92da4-125">INPUTS</span></span>

### <span data-ttu-id="92da4-126">없음</span><span class="sxs-lookup"><span data-stu-id="92da4-126">None</span></span>

## <span data-ttu-id="92da4-127">출력</span><span class="sxs-lookup"><span data-stu-id="92da4-127">OUTPUTS</span></span>

### <span data-ttu-id="92da4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="92da4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="92da4-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92da4-129">NOTES</span></span>

## <span data-ttu-id="92da4-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92da4-130">RELATED LINKS</span></span>
