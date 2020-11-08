---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044438"
---
# <span data-ttu-id="8b46f-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="8b46f-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="8b46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b46f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b46f-103">CosmosDB Gremlin 그래프를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="8b46f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b46f-104">SYNTAX</span></span>

### <span data-ttu-id="8b46f-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b46f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b46f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b46f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b46f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8b46f-107">DESCRIPTION</span></span>
<span data-ttu-id="8b46f-108">**Set-AzCosmosDBGremlinGraph** Cmdlet은 CosmosDB Gremlin Graph를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="8b46f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8b46f-109">EXAMPLES</span></span>

### <span data-ttu-id="8b46f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b46f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="8b46f-111">리소스 개체에는 IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="8b46f-112">변수</span><span class="sxs-lookup"><span data-stu-id="8b46f-112">PARAMETERS</span></span>

### <span data-ttu-id="8b46f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8b46f-113">-AccountName</span></span>
<span data-ttu-id="8b46f-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8b46f-115">-확인</span><span class="sxs-lookup"><span data-stu-id="8b46f-115">-Confirm</span></span>
<span data-ttu-id="8b46f-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b46f-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8b46f-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="8b46f-118">PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 제공 되는 경우 컨테이너의 ConflictResolutionPolicy로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b46f-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="8b46f-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="8b46f-120">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="8b46f-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="8b46f-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="8b46f-122">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="8b46f-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="8b46f-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="8b46f-124">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="8b46f-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8b46f-125">-DatabaseName</span></span>
<span data-ttu-id="8b46f-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-126">Database name.</span></span>

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

### <span data-ttu-id="8b46f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b46f-127">-DefaultProfile</span></span>
<span data-ttu-id="8b46f-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b46f-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="8b46f-129">-IndexingPolicy</span></span>
<span data-ttu-id="8b46f-130">CosmosDB Sqlindexingpolicy 유형의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b46f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b46f-131">-InputObject</span></span>
<span data-ttu-id="8b46f-132">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="8b46f-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="8b46f-133">-이름</span><span class="sxs-lookup"><span data-stu-id="8b46f-133">-Name</span></span>
<span data-ttu-id="8b46f-134">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="8b46f-135">-파티션 형식</span><span class="sxs-lookup"><span data-stu-id="8b46f-135">-PartitionKeyKind</span></span>
<span data-ttu-id="8b46f-136">분할에 사용 되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="8b46f-137">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="8b46f-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="8b46f-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="8b46f-138">-PartitionKeyPath</span></span>
<span data-ttu-id="8b46f-139">파티션 키 경로 (예: '/address/zipcode ').</span><span class="sxs-lookup"><span data-stu-id="8b46f-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b46f-140">-파티션 버전</span><span class="sxs-lookup"><span data-stu-id="8b46f-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="8b46f-141">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="8b46f-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="8b46f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b46f-142">-ResourceGroupName</span></span>
<span data-ttu-id="8b46f-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-143">Name of resource group.</span></span>

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

### <span data-ttu-id="8b46f-144">-처리량</span><span class="sxs-lookup"><span data-stu-id="8b46f-144">-Throughput</span></span>
<span data-ttu-id="8b46f-145">Gremlin 그래프의 처리량 (1/s)</span><span class="sxs-lookup"><span data-stu-id="8b46f-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="8b46f-146">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-146">Default value is 400.</span></span>

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

### <span data-ttu-id="8b46f-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="8b46f-147">-TtlInSeconds</span></span>
<span data-ttu-id="8b46f-148">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="8b46f-149">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="8b46f-150">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="8b46f-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8b46f-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="8b46f-152">UniqueKeyPolicy. CosmosDB. PSSqlUniqueKeyPolicy의 형식 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b46f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b46f-153">-WhatIf</span></span>
<span data-ttu-id="8b46f-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b46f-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b46f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b46f-156">CommonParameters</span></span>
<span data-ttu-id="8b46f-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b46f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b46f-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b46f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b46f-159">입력</span><span class="sxs-lookup"><span data-stu-id="8b46f-159">INPUTS</span></span>

### <span data-ttu-id="8b46f-160">CosmosDB. a m a. m 인덱스 Ingpolicy</span><span class="sxs-lookup"><span data-stu-id="8b46f-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="8b46f-161">CosmosDB. PSUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="8b46f-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="8b46f-162">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="8b46f-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="8b46f-163">출력</span><span class="sxs-lookup"><span data-stu-id="8b46f-163">OUTPUTS</span></span>

### <span data-ttu-id="8b46f-164">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="8b46f-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="8b46f-165">상속자</span><span class="sxs-lookup"><span data-stu-id="8b46f-165">NOTES</span></span>

## <span data-ttu-id="8b46f-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b46f-166">RELATED LINKS</span></span>
