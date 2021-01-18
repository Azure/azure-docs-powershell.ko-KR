---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495797"
---
# <span data-ttu-id="ceec6-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="ceec6-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="ceec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceec6-102">SYNOPSIS</span></span>
<span data-ttu-id="ceec6-103">PSIndexes 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="ceec6-104">Set-AzCosmosDBGremlinIncludedPath에 대한 매개 변수 값으로 전달될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="ceec6-105">구문</span><span class="sxs-lookup"><span data-stu-id="ceec6-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceec6-106">설명</span><span class="sxs-lookup"><span data-stu-id="ceec6-106">DESCRIPTION</span></span>
<span data-ttu-id="ceec6-107">Gremlin API의 IncludedPath 인덱스에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="ceec6-108">예제</span><span class="sxs-lookup"><span data-stu-id="ceec6-108">EXAMPLES</span></span>

### <span data-ttu-id="ceec6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ceec6-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="ceec6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceec6-110">PARAMETERS</span></span>

### <span data-ttu-id="ceec6-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="ceec6-111">-DataType</span></span>
<span data-ttu-id="ceec6-112">인덱싱 동작이 적용되는 데이터 스타일입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="ceec6-113">가능한 값은 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="ceec6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceec6-114">-DefaultProfile</span></span>
<span data-ttu-id="ceec6-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceec6-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="ceec6-116">-Kind</span></span>
<span data-ttu-id="ceec6-117">인덱스의 형식을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-117">Indicates the type of index.</span></span>
<span data-ttu-id="ceec6-118">가능한 값은 'Hash', 'Range', 'Spatial'입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="ceec6-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="ceec6-119">-Precision</span></span>
<span data-ttu-id="ceec6-120">인덱스의 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-120">The precision of the index.</span></span>
<span data-ttu-id="ceec6-121">-1은 최대 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="ceec6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceec6-122">CommonParameters</span></span>
<span data-ttu-id="ceec6-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ceec6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceec6-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ceec6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceec6-125">입력</span><span class="sxs-lookup"><span data-stu-id="ceec6-125">INPUTS</span></span>

### <span data-ttu-id="ceec6-126">없음</span><span class="sxs-lookup"><span data-stu-id="ceec6-126">None</span></span>

## <span data-ttu-id="ceec6-127">출력</span><span class="sxs-lookup"><span data-stu-id="ceec6-127">OUTPUTS</span></span>

### <span data-ttu-id="ceec6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span><span class="sxs-lookup"><span data-stu-id="ceec6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="ceec6-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ceec6-129">NOTES</span></span>

## <span data-ttu-id="ceec6-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceec6-130">RELATED LINKS</span></span>
