---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044437"
---
# <span data-ttu-id="24d20-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="24d20-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="24d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d20-102">SYNOPSIS</span></span>
<span data-ttu-id="24d20-103">CosmosDB MongoDB Collection을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="24d20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24d20-104">SYNTAX</span></span>

### <span data-ttu-id="24d20-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="24d20-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d20-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24d20-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d20-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24d20-107">DESCRIPTION</span></span>
<span data-ttu-id="24d20-108">**Set-AzCosmosDBMongoDBCollection** Cmdlet은 CosmosDB MongoDB 컬렉션을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="24d20-109">예제의</span><span class="sxs-lookup"><span data-stu-id="24d20-109">EXAMPLES</span></span>

### <span data-ttu-id="24d20-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="24d20-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="24d20-111">리소스 개체에 MongoIndexes, _rid, _ts _etag 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="24d20-112">변수</span><span class="sxs-lookup"><span data-stu-id="24d20-112">PARAMETERS</span></span>

### <span data-ttu-id="24d20-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24d20-113">-AccountName</span></span>
<span data-ttu-id="24d20-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24d20-115">-확인</span><span class="sxs-lookup"><span data-stu-id="24d20-115">-Confirm</span></span>
<span data-ttu-id="24d20-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d20-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24d20-117">-DatabaseName</span></span>
<span data-ttu-id="24d20-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-118">Database name.</span></span>

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

### <span data-ttu-id="24d20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d20-119">-DefaultProfile</span></span>
<span data-ttu-id="24d20-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d20-121">-인덱스</span><span class="sxs-lookup"><span data-stu-id="24d20-121">-Index</span></span>
<span data-ttu-id="24d20-122">PSMongoIndex 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-122">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d20-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24d20-123">-InputObject</span></span>
<span data-ttu-id="24d20-124">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24d20-125">-이름</span><span class="sxs-lookup"><span data-stu-id="24d20-125">-Name</span></span>
<span data-ttu-id="24d20-126">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-126">Collection name.</span></span>

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

### <span data-ttu-id="24d20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d20-127">-ResourceGroupName</span></span>
<span data-ttu-id="24d20-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-128">Name of resource group.</span></span>

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

### <span data-ttu-id="24d20-129">-샤 드</span><span class="sxs-lookup"><span data-stu-id="24d20-129">-Shard</span></span>
<span data-ttu-id="24d20-130">Sharding 키 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-130">Sharding key path.</span></span>

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

### <span data-ttu-id="24d20-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="24d20-131">-Throughput</span></span>
<span data-ttu-id="24d20-132">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="24d20-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-133">Default value is 400.</span></span>

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

### <span data-ttu-id="24d20-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d20-134">-WhatIf</span></span>
<span data-ttu-id="24d20-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d20-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d20-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d20-137">CommonParameters</span></span>
<span data-ttu-id="24d20-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d20-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d20-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24d20-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d20-140">입력</span><span class="sxs-lookup"><span data-stu-id="24d20-140">INPUTS</span></span>

### <span data-ttu-id="24d20-141">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="24d20-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="24d20-142">출력</span><span class="sxs-lookup"><span data-stu-id="24d20-142">OUTPUTS</span></span>

### <span data-ttu-id="24d20-143">CosmosDB. PSMongoDBCollectionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="24d20-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="24d20-144">상속자</span><span class="sxs-lookup"><span data-stu-id="24d20-144">NOTES</span></span>

## <span data-ttu-id="24d20-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24d20-145">RELATED LINKS</span></span>
