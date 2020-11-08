---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044122"
---
# <span data-ttu-id="b0578-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b0578-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b0578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0578-102">SYNOPSIS</span></span>
<span data-ttu-id="b0578-103">CosmosDB Gremlin 그래프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b0578-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0578-104">SYNTAX</span></span>

### <span data-ttu-id="b0578-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0578-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="b0578-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0578-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0578-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0578-107">DESCRIPTION</span></span>
<span data-ttu-id="b0578-108">**AzCosmosDBGremlinGraph** Cmdlet은 CosmosDB Gremlin 그래프 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="b0578-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b0578-109">EXAMPLES</span></span>

### <span data-ttu-id="b0578-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0578-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="b0578-111">리소스 개체에는 IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b0578-112">변수</span><span class="sxs-lookup"><span data-stu-id="b0578-112">PARAMETERS</span></span>

### <span data-ttu-id="b0578-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0578-113">-AccountName</span></span>
<span data-ttu-id="b0578-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0578-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0578-115">-DatabaseName</span></span>
<span data-ttu-id="b0578-116">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-116">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0578-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0578-117">-DefaultProfile</span></span>
<span data-ttu-id="b0578-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0578-119">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="b0578-119">-Detailed</span></span>
<span data-ttu-id="b0578-120">그런 다음 cmdlet은 해당 하는 처리 값을 사용 하 여 Gremlin 그래프를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0578-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0578-121">-InputObject</span></span>
<span data-ttu-id="b0578-122">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="b0578-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0578-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b0578-123">-Name</span></span>
<span data-ttu-id="b0578-124">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b0578-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0578-125">-ResourceGroupName</span></span>
<span data-ttu-id="b0578-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-126">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0578-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0578-127">CommonParameters</span></span>
<span data-ttu-id="b0578-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0578-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0578-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0578-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0578-130">입력</span><span class="sxs-lookup"><span data-stu-id="b0578-130">INPUTS</span></span>

### <span data-ttu-id="b0578-131">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="b0578-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b0578-132">출력</span><span class="sxs-lookup"><span data-stu-id="b0578-132">OUTPUTS</span></span>

### <span data-ttu-id="b0578-133">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="b0578-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="b0578-134">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="b0578-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b0578-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b0578-135">NOTES</span></span>

## <span data-ttu-id="b0578-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0578-136">RELATED LINKS</span></span>
