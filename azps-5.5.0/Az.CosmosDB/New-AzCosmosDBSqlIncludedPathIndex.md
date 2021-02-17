---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209845"
---
# <span data-ttu-id="3a1b7-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="3a1b7-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="3a1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1b7-103">PSIndexes 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="3a1b7-104">Set-AzCosmosDBSqlIncludedPath에 대한 매개 변수 값으로 전달될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="3a1b7-105">구문</span><span class="sxs-lookup"><span data-stu-id="3a1b7-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a1b7-106">설명</span><span class="sxs-lookup"><span data-stu-id="3a1b7-106">DESCRIPTION</span></span>
<span data-ttu-id="3a1b7-107">Sql API의 IncludedPath 인덱스에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="3a1b7-108">예제</span><span class="sxs-lookup"><span data-stu-id="3a1b7-108">EXAMPLES</span></span>

### <span data-ttu-id="3a1b7-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a1b7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="3a1b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a1b7-110">PARAMETERS</span></span>

### <span data-ttu-id="3a1b7-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="3a1b7-111">-DataType</span></span>
<span data-ttu-id="3a1b7-112">인덱싱 동작이 적용되는 데이터형입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="3a1b7-113">가능한 값은 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="3a1b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1b7-114">-DefaultProfile</span></span>
<span data-ttu-id="3a1b7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1b7-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="3a1b7-116">-Kind</span></span>
<span data-ttu-id="3a1b7-117">인덱스의 형식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-117">Indicates the type of index.</span></span>
<span data-ttu-id="3a1b7-118">가능한 값은 'Hash', 'Range', 'Spatial'입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="3a1b7-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="3a1b7-119">-Precision</span></span>
<span data-ttu-id="3a1b7-120">인덱스의 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-120">The precision of the index.</span></span>
<span data-ttu-id="3a1b7-121">-1은 최대 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="3a1b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1b7-122">CommonParameters</span></span>
<span data-ttu-id="3a1b7-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1b7-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1b7-125">입력</span><span class="sxs-lookup"><span data-stu-id="3a1b7-125">INPUTS</span></span>

### <span data-ttu-id="3a1b7-126">없음</span><span class="sxs-lookup"><span data-stu-id="3a1b7-126">None</span></span>

## <span data-ttu-id="3a1b7-127">출력</span><span class="sxs-lookup"><span data-stu-id="3a1b7-127">OUTPUTS</span></span>

### <span data-ttu-id="3a1b7-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="3a1b7-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="3a1b7-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a1b7-129">NOTES</span></span>

## <span data-ttu-id="3a1b7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a1b7-130">RELATED LINKS</span></span>
