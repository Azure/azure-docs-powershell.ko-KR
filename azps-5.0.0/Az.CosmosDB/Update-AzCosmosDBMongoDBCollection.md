---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306785"
---
# <span data-ttu-id="b3157-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="b3157-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="b3157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3157-102">SYNOPSIS</span></span>
<span data-ttu-id="b3157-103">CosmosDB MongoDB Collection을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="b3157-104">기존 컬렉션을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="b3157-105">구문과</span><span class="sxs-lookup"><span data-stu-id="b3157-105">SYNTAX</span></span>

### <span data-ttu-id="b3157-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3157-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3157-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3157-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3157-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3157-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3157-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b3157-109">DESCRIPTION</span></span>
<span data-ttu-id="b3157-110">CosmosDB MongoDB Collection을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="b3157-111">기존 컬렉션을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="b3157-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b3157-112">EXAMPLES</span></span>

### <span data-ttu-id="b3157-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3157-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="b3157-114">변수</span><span class="sxs-lookup"><span data-stu-id="b3157-114">PARAMETERS</span></span>

### <span data-ttu-id="b3157-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3157-115">-AccountName</span></span>
<span data-ttu-id="b3157-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3157-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="b3157-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="b3157-118">분석 저장소에 대 한 TTL</span><span class="sxs-lookup"><span data-stu-id="b3157-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="b3157-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b3157-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b3157-120">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b3157-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b3157-121">-Confirm</span></span>
<span data-ttu-id="b3157-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3157-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3157-123">-DatabaseName</span></span>
<span data-ttu-id="b3157-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-124">Database name.</span></span>

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

### <span data-ttu-id="b3157-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3157-125">-DefaultProfile</span></span>
<span data-ttu-id="b3157-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3157-127">-인덱스</span><span class="sxs-lookup"><span data-stu-id="b3157-127">-Index</span></span>
<span data-ttu-id="b3157-128">PSMongoIndex 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="b3157-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3157-129">-InputObject</span></span>
<span data-ttu-id="b3157-130">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="b3157-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3157-131">-이름</span><span class="sxs-lookup"><span data-stu-id="b3157-131">-Name</span></span>
<span data-ttu-id="b3157-132">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-132">Collection name.</span></span>

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

### <span data-ttu-id="b3157-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b3157-133">-ParentObject</span></span>
<span data-ttu-id="b3157-134">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="b3157-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3157-135">-ResourceGroupName</span></span>
<span data-ttu-id="b3157-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-136">Name of resource group.</span></span>

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

### <span data-ttu-id="b3157-137">-샤 드</span><span class="sxs-lookup"><span data-stu-id="b3157-137">-Shard</span></span>
<span data-ttu-id="b3157-138">Sharding 키 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-138">Sharding key path.</span></span>

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

### <span data-ttu-id="b3157-139">-처리량</span><span class="sxs-lookup"><span data-stu-id="b3157-139">-Throughput</span></span>
<span data-ttu-id="b3157-140">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="b3157-141">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-141">Default value is 400.</span></span>

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

### <span data-ttu-id="b3157-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3157-142">-WhatIf</span></span>
<span data-ttu-id="b3157-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3157-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3157-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3157-145">CommonParameters</span></span>
<span data-ttu-id="b3157-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3157-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3157-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3157-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3157-148">입력</span><span class="sxs-lookup"><span data-stu-id="b3157-148">INPUTS</span></span>

### <span data-ttu-id="b3157-149">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="b3157-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="b3157-150">CosmosDB. PSMongoDBCollectionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="b3157-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="b3157-151">출력</span><span class="sxs-lookup"><span data-stu-id="b3157-151">OUTPUTS</span></span>

### <span data-ttu-id="b3157-152">CosmosDB. PSMongoDBCollectionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="b3157-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="b3157-153">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="b3157-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b3157-154">상속자</span><span class="sxs-lookup"><span data-stu-id="b3157-154">NOTES</span></span>

## <span data-ttu-id="b3157-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3157-155">RELATED LINKS</span></span>
