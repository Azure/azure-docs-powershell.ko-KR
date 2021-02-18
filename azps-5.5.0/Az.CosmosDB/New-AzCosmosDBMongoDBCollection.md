---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181313"
---
# <span data-ttu-id="3cb39-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="3cb39-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="3cb39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb39-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb39-103">새 CosmosDB MongoDB 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="3cb39-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cb39-104">SYNTAX</span></span>

### <span data-ttu-id="3cb39-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3cb39-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb39-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cb39-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cb39-107">설명</span><span class="sxs-lookup"><span data-stu-id="3cb39-107">DESCRIPTION</span></span>
<span data-ttu-id="3cb39-108">새 CosmosDB MongoDB 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="3cb39-109">예제</span><span class="sxs-lookup"><span data-stu-id="3cb39-109">EXAMPLES</span></span>

### <span data-ttu-id="3cb39-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cb39-110">Example 1</span></span>
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

## <span data-ttu-id="3cb39-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cb39-111">PARAMETERS</span></span>

### <span data-ttu-id="3cb39-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cb39-112">-AccountName</span></span>
<span data-ttu-id="3cb39-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3cb39-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="3cb39-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="3cb39-115">분석 저장소에 대한 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="3cb39-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3cb39-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3cb39-117">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3cb39-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cb39-118">-Confirm</span></span>
<span data-ttu-id="3cb39-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb39-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3cb39-120">-DatabaseName</span></span>
<span data-ttu-id="3cb39-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-121">Database name.</span></span>

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

### <span data-ttu-id="3cb39-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb39-122">-DefaultProfile</span></span>
<span data-ttu-id="3cb39-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb39-124">-Index</span><span class="sxs-lookup"><span data-stu-id="3cb39-124">-Index</span></span>
<span data-ttu-id="3cb39-125">PSMongoIndex 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="3cb39-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3cb39-126">-Name</span></span>
<span data-ttu-id="3cb39-127">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-127">Collection name.</span></span>

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

### <span data-ttu-id="3cb39-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3cb39-128">-ParentObject</span></span>
<span data-ttu-id="3cb39-129">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="3cb39-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb39-130">-ResourceGroupName</span></span>
<span data-ttu-id="3cb39-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-131">Name of resource group.</span></span>

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

### <span data-ttu-id="3cb39-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="3cb39-132">-Shard</span></span>
<span data-ttu-id="3cb39-133">키 경로의 Sharding 키입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-133">Sharding key path.</span></span>

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

### <span data-ttu-id="3cb39-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="3cb39-134">-Throughput</span></span>
<span data-ttu-id="3cb39-135">컨테이너의 SQL(RU/s)</span><span class="sxs-lookup"><span data-stu-id="3cb39-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="3cb39-136">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-136">Default value is 400.</span></span>

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

### <span data-ttu-id="3cb39-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb39-137">-WhatIf</span></span>
<span data-ttu-id="3cb39-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3cb39-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb39-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb39-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb39-140">CommonParameters</span></span>
<span data-ttu-id="3cb39-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb39-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb39-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cb39-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb39-143">입력</span><span class="sxs-lookup"><span data-stu-id="3cb39-143">INPUTS</span></span>

### <span data-ttu-id="3cb39-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3cb39-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3cb39-145">출력</span><span class="sxs-lookup"><span data-stu-id="3cb39-145">OUTPUTS</span></span>

### <span data-ttu-id="3cb39-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="3cb39-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="3cb39-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="3cb39-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="3cb39-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cb39-148">NOTES</span></span>

## <span data-ttu-id="3cb39-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cb39-149">RELATED LINKS</span></span>
