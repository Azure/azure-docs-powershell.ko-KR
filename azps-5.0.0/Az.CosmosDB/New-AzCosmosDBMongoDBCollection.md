---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307043"
---
# <span data-ttu-id="766a2-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="766a2-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="766a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766a2-102">SYNOPSIS</span></span>
<span data-ttu-id="766a2-103">새 CosmosDB MongoDB Collection을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="766a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="766a2-104">SYNTAX</span></span>

### <span data-ttu-id="766a2-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="766a2-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="766a2-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="766a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="766a2-107">DESCRIPTION</span></span>
<span data-ttu-id="766a2-108">새 CosmosDB MongoDB Collection을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="766a2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="766a2-109">EXAMPLES</span></span>

### <span data-ttu-id="766a2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="766a2-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="766a2-111">변수</span><span class="sxs-lookup"><span data-stu-id="766a2-111">PARAMETERS</span></span>

### <span data-ttu-id="766a2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="766a2-112">-AccountName</span></span>
<span data-ttu-id="766a2-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="766a2-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="766a2-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="766a2-115">분석 저장소에 대 한 TTL</span><span class="sxs-lookup"><span data-stu-id="766a2-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="766a2-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="766a2-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="766a2-117">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="766a2-118">-확인</span><span class="sxs-lookup"><span data-stu-id="766a2-118">-Confirm</span></span>
<span data-ttu-id="766a2-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766a2-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="766a2-120">-DatabaseName</span></span>
<span data-ttu-id="766a2-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-121">Database name.</span></span>

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

### <span data-ttu-id="766a2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766a2-122">-DefaultProfile</span></span>
<span data-ttu-id="766a2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="766a2-124">-인덱스</span><span class="sxs-lookup"><span data-stu-id="766a2-124">-Index</span></span>
<span data-ttu-id="766a2-125">PSMongoIndex 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="766a2-126">-이름</span><span class="sxs-lookup"><span data-stu-id="766a2-126">-Name</span></span>
<span data-ttu-id="766a2-127">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-127">Collection name.</span></span>

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

### <span data-ttu-id="766a2-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="766a2-128">-ParentObject</span></span>
<span data-ttu-id="766a2-129">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="766a2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766a2-130">-ResourceGroupName</span></span>
<span data-ttu-id="766a2-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-131">Name of resource group.</span></span>

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

### <span data-ttu-id="766a2-132">-샤 드</span><span class="sxs-lookup"><span data-stu-id="766a2-132">-Shard</span></span>
<span data-ttu-id="766a2-133">Sharding 키 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-133">Sharding key path.</span></span>

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

### <span data-ttu-id="766a2-134">-처리량</span><span class="sxs-lookup"><span data-stu-id="766a2-134">-Throughput</span></span>
<span data-ttu-id="766a2-135">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="766a2-136">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-136">Default value is 400.</span></span>

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

### <span data-ttu-id="766a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766a2-137">-WhatIf</span></span>
<span data-ttu-id="766a2-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="766a2-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766a2-140">CommonParameters</span></span>
<span data-ttu-id="766a2-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="766a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766a2-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="766a2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766a2-143">입력</span><span class="sxs-lookup"><span data-stu-id="766a2-143">INPUTS</span></span>

### <span data-ttu-id="766a2-144">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="766a2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="766a2-145">출력</span><span class="sxs-lookup"><span data-stu-id="766a2-145">OUTPUTS</span></span>

### <span data-ttu-id="766a2-146">CosmosDB. PSMongoDBCollectionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="766a2-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="766a2-147">CosmosDB (ConflictingResourceException).</span><span class="sxs-lookup"><span data-stu-id="766a2-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="766a2-148">상속자</span><span class="sxs-lookup"><span data-stu-id="766a2-148">NOTES</span></span>

## <span data-ttu-id="766a2-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="766a2-149">RELATED LINKS</span></span>
