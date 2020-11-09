---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306767"
---
# <span data-ttu-id="340d1-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="340d1-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="340d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340d1-102">SYNOPSIS</span></span>
<span data-ttu-id="340d1-103">CosmosDB Sql 컨테이너를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="340d1-104">기존 컨테이너를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="340d1-105">구문과</span><span class="sxs-lookup"><span data-stu-id="340d1-105">SYNTAX</span></span>

### <span data-ttu-id="340d1-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="340d1-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340d1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="340d1-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="340d1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="340d1-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="340d1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="340d1-109">DESCRIPTION</span></span>
<span data-ttu-id="340d1-110">CosmosDB Sql 컨테이너를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="340d1-111">기존 컨테이너를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="340d1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="340d1-112">EXAMPLES</span></span>

### <span data-ttu-id="340d1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="340d1-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="340d1-114">변수</span><span class="sxs-lookup"><span data-stu-id="340d1-114">PARAMETERS</span></span>

### <span data-ttu-id="340d1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="340d1-115">-AccountName</span></span>
<span data-ttu-id="340d1-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="340d1-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="340d1-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="340d1-118">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="340d1-119">-확인</span><span class="sxs-lookup"><span data-stu-id="340d1-119">-Confirm</span></span>
<span data-ttu-id="340d1-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="340d1-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="340d1-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="340d1-122">PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 제공 되는 경우 컨테이너의 ConflictResolutionPolicy로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340d1-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="340d1-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="340d1-124">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="340d1-125">ConflictResolutionPolicy 매개 변수와 함께 제공 된 경우이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="340d1-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="340d1-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="340d1-127">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="340d1-128">ConflictResolutionPolicy 매개 변수와 함께 제공 된 경우이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="340d1-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="340d1-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="340d1-130">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="340d1-131">ConflictResolutionPolicy 매개 변수와 함께 제공 된 경우이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="340d1-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="340d1-132">-DatabaseName</span></span>
<span data-ttu-id="340d1-133">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-133">Database name.</span></span>

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

### <span data-ttu-id="340d1-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340d1-134">-DefaultProfile</span></span>
<span data-ttu-id="340d1-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340d1-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="340d1-136">-IndexingPolicy</span></span>
<span data-ttu-id="340d1-137">CosmosDB Sqlindexingpolicy 유형의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340d1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="340d1-138">-InputObject</span></span>
<span data-ttu-id="340d1-139">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="340d1-139">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340d1-140">-이름</span><span class="sxs-lookup"><span data-stu-id="340d1-140">-Name</span></span>
<span data-ttu-id="340d1-141">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-141">Container name.</span></span>

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

### <span data-ttu-id="340d1-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="340d1-142">-ParentObject</span></span>
<span data-ttu-id="340d1-143">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="340d1-143">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340d1-144">-파티션 형식</span><span class="sxs-lookup"><span data-stu-id="340d1-144">-PartitionKeyKind</span></span>
<span data-ttu-id="340d1-145">분할에 사용 되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="340d1-146">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="340d1-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="340d1-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="340d1-147">-PartitionKeyPath</span></span>
<span data-ttu-id="340d1-148">파티션 키 경로 (예: '/address/zipcode ').</span><span class="sxs-lookup"><span data-stu-id="340d1-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340d1-149">-파티션 버전</span><span class="sxs-lookup"><span data-stu-id="340d1-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="340d1-150">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="340d1-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="340d1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340d1-151">-ResourceGroupName</span></span>
<span data-ttu-id="340d1-152">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-152">Name of resource group.</span></span>

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

### <span data-ttu-id="340d1-153">-처리량</span><span class="sxs-lookup"><span data-stu-id="340d1-153">-Throughput</span></span>
<span data-ttu-id="340d1-154">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="340d1-155">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-155">Default value is 400.</span></span>

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

### <span data-ttu-id="340d1-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="340d1-156">-TtlInSeconds</span></span>
<span data-ttu-id="340d1-157">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="340d1-158">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="340d1-159">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="340d1-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="340d1-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="340d1-161">UniqueKeyPolicy. CosmosDB. PSSqlUniqueKeyPolicy의 형식 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340d1-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="340d1-162">-WhatIf</span></span>
<span data-ttu-id="340d1-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="340d1-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="340d1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340d1-165">CommonParameters</span></span>
<span data-ttu-id="340d1-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="340d1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340d1-167">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="340d1-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340d1-168">입력</span><span class="sxs-lookup"><span data-stu-id="340d1-168">INPUTS</span></span>

### <span data-ttu-id="340d1-169">CosmosDB. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="340d1-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="340d1-170">CosmosDB. PSSqlUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="340d1-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="340d1-171">CosmosDB. PSSqlConflictResolutionPolicy/.</span><span class="sxs-lookup"><span data-stu-id="340d1-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="340d1-172">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="340d1-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="340d1-173">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="340d1-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="340d1-174">출력</span><span class="sxs-lookup"><span data-stu-id="340d1-174">OUTPUTS</span></span>

### <span data-ttu-id="340d1-175">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="340d1-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="340d1-176">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="340d1-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="340d1-177">상속자</span><span class="sxs-lookup"><span data-stu-id="340d1-177">NOTES</span></span>

## <span data-ttu-id="340d1-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="340d1-178">RELATED LINKS</span></span>
