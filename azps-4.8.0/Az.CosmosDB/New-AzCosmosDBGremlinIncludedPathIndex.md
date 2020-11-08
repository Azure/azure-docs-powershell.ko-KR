---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056458"
---
# <span data-ttu-id="8e498-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="8e498-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="8e498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e498-102">SYNOPSIS</span></span>
<span data-ttu-id="8e498-103">PSIndexes 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="8e498-104">Set-AzCosmosDBGremlinIncludedPath에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="8e498-105">구문과</span><span class="sxs-lookup"><span data-stu-id="8e498-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e498-106">설명은</span><span class="sxs-lookup"><span data-stu-id="8e498-106">DESCRIPTION</span></span>
<span data-ttu-id="8e498-107">Gremlin API의 IncludedPath's 인덱스에 해당 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="8e498-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8e498-108">EXAMPLES</span></span>

### <span data-ttu-id="8e498-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e498-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="8e498-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e498-110">PARAMETERS</span></span>

### <span data-ttu-id="8e498-111">-DataType</span><span class="sxs-lookup"><span data-stu-id="8e498-111">-DataType</span></span>
<span data-ttu-id="8e498-112">인덱싱 동작이 적용 되는 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="8e498-113">사용할 수 있는 값으로는 ' String ', ' Number ', ' 요점 ', ' Polygon ', ' LineString ', ' MultiPolygon '이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="8e498-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e498-114">-DefaultProfile</span></span>
<span data-ttu-id="8e498-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e498-116">-종류</span><span class="sxs-lookup"><span data-stu-id="8e498-116">-Kind</span></span>
<span data-ttu-id="8e498-117">인덱스 유형을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-117">Indicates the type of index.</span></span>
<span data-ttu-id="8e498-118">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range ', ' 공간 '</span><span class="sxs-lookup"><span data-stu-id="8e498-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="8e498-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="8e498-119">-Precision</span></span>
<span data-ttu-id="8e498-120">인덱스의 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-120">The precision of the index.</span></span>
<span data-ttu-id="8e498-121">-1은 최대 정밀도입니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="8e498-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e498-122">CommonParameters</span></span>
<span data-ttu-id="8e498-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e498-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e498-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e498-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e498-125">입력</span><span class="sxs-lookup"><span data-stu-id="8e498-125">INPUTS</span></span>

### <span data-ttu-id="8e498-126">않아야</span><span class="sxs-lookup"><span data-stu-id="8e498-126">None</span></span>

## <span data-ttu-id="8e498-127">출력</span><span class="sxs-lookup"><span data-stu-id="8e498-127">OUTPUTS</span></span>

### <span data-ttu-id="8e498-128">CosmosDB. a m a. a m a. PSIndexes</span><span class="sxs-lookup"><span data-stu-id="8e498-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="8e498-129">상속자</span><span class="sxs-lookup"><span data-stu-id="8e498-129">NOTES</span></span>

## <span data-ttu-id="8e498-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e498-130">RELATED LINKS</span></span>
