---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983627"
---
# <span data-ttu-id="8444d-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="8444d-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="8444d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8444d-102">SYNOPSIS</span></span>
<span data-ttu-id="8444d-103">CosmosDB Gremlin Graph를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="8444d-104">구문</span><span class="sxs-lookup"><span data-stu-id="8444d-104">SYNTAX</span></span>

### <span data-ttu-id="8444d-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8444d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="8444d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8444d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8444d-107">설명</span><span class="sxs-lookup"><span data-stu-id="8444d-107">DESCRIPTION</span></span>
<span data-ttu-id="8444d-108">**Get-AzCosmosDBGremlinGraph** cmdlet은 CosmosDB Gremlin Graph 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="8444d-109">예제</span><span class="sxs-lookup"><span data-stu-id="8444d-109">EXAMPLES</span></span>

### <span data-ttu-id="8444d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8444d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="8444d-111">리소스 개체에는 IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="8444d-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="8444d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8444d-112">PARAMETERS</span></span>

### <span data-ttu-id="8444d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8444d-113">-AccountName</span></span>
<span data-ttu-id="8444d-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8444d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8444d-115">-DatabaseName</span></span>
<span data-ttu-id="8444d-116">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-116">Database name.</span></span>

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

### <span data-ttu-id="8444d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8444d-117">-DefaultProfile</span></span>
<span data-ttu-id="8444d-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8444d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8444d-119">-Name</span></span>
<span data-ttu-id="8444d-120">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="8444d-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8444d-121">-ParentObject</span></span>
<span data-ttu-id="8444d-122">Gremlin Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="8444d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8444d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8444d-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-124">Name of resource group.</span></span>

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

### <span data-ttu-id="8444d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8444d-125">CommonParameters</span></span>
<span data-ttu-id="8444d-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8444d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8444d-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8444d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8444d-128">입력</span><span class="sxs-lookup"><span data-stu-id="8444d-128">INPUTS</span></span>

### <span data-ttu-id="8444d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8444d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="8444d-130">출력</span><span class="sxs-lookup"><span data-stu-id="8444d-130">OUTPUTS</span></span>

### <span data-ttu-id="8444d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="8444d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="8444d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8444d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8444d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8444d-133">NOTES</span></span>

## <span data-ttu-id="8444d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8444d-134">RELATED LINKS</span></span>
