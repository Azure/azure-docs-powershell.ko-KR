---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 3864693c5fd6da8c96557aac6f1626329f4e906f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954768"
---
# <span data-ttu-id="65a1e-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="65a1e-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="65a1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="65a1e-103">새 CosmosDB MongoDB 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="65a1e-104">구문</span><span class="sxs-lookup"><span data-stu-id="65a1e-104">SYNTAX</span></span>

### <span data-ttu-id="65a1e-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="65a1e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65a1e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65a1e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65a1e-107">설명</span><span class="sxs-lookup"><span data-stu-id="65a1e-107">DESCRIPTION</span></span>
<span data-ttu-id="65a1e-108">새 CosmosDB MongoDB 컬렉션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="65a1e-109">예제</span><span class="sxs-lookup"><span data-stu-id="65a1e-109">EXAMPLES</span></span>

### <span data-ttu-id="65a1e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="65a1e-110">Example 1</span></span>
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

## <span data-ttu-id="65a1e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65a1e-111">PARAMETERS</span></span>

### <span data-ttu-id="65a1e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65a1e-112">-AccountName</span></span>
<span data-ttu-id="65a1e-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65a1e-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="65a1e-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="65a1e-115">분석 저장소용 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="65a1e-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="65a1e-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="65a1e-117">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="65a1e-118">-확인</span><span class="sxs-lookup"><span data-stu-id="65a1e-118">-Confirm</span></span>
<span data-ttu-id="65a1e-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a1e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65a1e-120">-DatabaseName</span></span>
<span data-ttu-id="65a1e-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-121">Database name.</span></span>

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

### <span data-ttu-id="65a1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a1e-122">-DefaultProfile</span></span>
<span data-ttu-id="65a1e-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65a1e-124">-Index</span><span class="sxs-lookup"><span data-stu-id="65a1e-124">-Index</span></span>
<span data-ttu-id="65a1e-125">PSMongoIndex 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="65a1e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="65a1e-126">-Name</span></span>
<span data-ttu-id="65a1e-127">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-127">Collection name.</span></span>

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

### <span data-ttu-id="65a1e-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="65a1e-128">-ParentObject</span></span>
<span data-ttu-id="65a1e-129">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="65a1e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a1e-130">-ResourceGroupName</span></span>
<span data-ttu-id="65a1e-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-131">Name of resource group.</span></span>

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

### <span data-ttu-id="65a1e-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="65a1e-132">-Shard</span></span>
<span data-ttu-id="65a1e-133">키 경로의 셰이드링</span><span class="sxs-lookup"><span data-stu-id="65a1e-133">Sharding key path.</span></span>

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

### <span data-ttu-id="65a1e-134">-Throughput</span><span class="sxs-lookup"><span data-stu-id="65a1e-134">-Throughput</span></span>
<span data-ttu-id="65a1e-135">RU/s SQL 컨테이너의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="65a1e-136">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-136">Default value is 400.</span></span>

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

### <span data-ttu-id="65a1e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a1e-137">-WhatIf</span></span>
<span data-ttu-id="65a1e-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a1e-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a1e-140">CommonParameters</span></span>
<span data-ttu-id="65a1e-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65a1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a1e-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65a1e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a1e-143">입력</span><span class="sxs-lookup"><span data-stu-id="65a1e-143">INPUTS</span></span>

### <span data-ttu-id="65a1e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="65a1e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="65a1e-145">출력</span><span class="sxs-lookup"><span data-stu-id="65a1e-145">OUTPUTS</span></span>

### <span data-ttu-id="65a1e-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="65a1e-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="65a1e-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="65a1e-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="65a1e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65a1e-148">NOTES</span></span>

## <span data-ttu-id="65a1e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65a1e-149">RELATED LINKS</span></span>
