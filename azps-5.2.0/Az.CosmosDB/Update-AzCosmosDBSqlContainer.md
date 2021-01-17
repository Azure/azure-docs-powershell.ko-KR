---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371715"
---
# <span data-ttu-id="145bf-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="145bf-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="145bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145bf-102">SYNOPSIS</span></span>
<span data-ttu-id="145bf-103">CosmosDB Sql 컨테이너를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="145bf-104">기존 컨테이너를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="145bf-105">구문</span><span class="sxs-lookup"><span data-stu-id="145bf-105">SYNTAX</span></span>

### <span data-ttu-id="145bf-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="145bf-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="145bf-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="145bf-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="145bf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="145bf-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145bf-109">설명</span><span class="sxs-lookup"><span data-stu-id="145bf-109">DESCRIPTION</span></span>
<span data-ttu-id="145bf-110">CosmosDB Sql 컨테이너를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="145bf-111">기존 컨테이너를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="145bf-112">예제</span><span class="sxs-lookup"><span data-stu-id="145bf-112">EXAMPLES</span></span>

### <span data-ttu-id="145bf-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="145bf-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="145bf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="145bf-114">PARAMETERS</span></span>

### <span data-ttu-id="145bf-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="145bf-115">-AccountName</span></span>
<span data-ttu-id="145bf-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="145bf-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="145bf-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="145bf-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="145bf-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="145bf-119">-Confirm</span></span>
<span data-ttu-id="145bf-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145bf-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="145bf-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="145bf-122">제공된 경우 PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체가 컨테이너의 ConflictResolutionPolicy로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="145bf-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="145bf-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="145bf-124">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="145bf-125">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="145bf-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="145bf-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="145bf-127">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="145bf-128">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="145bf-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="145bf-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="145bf-130">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="145bf-131">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="145bf-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="145bf-132">-DatabaseName</span></span>
<span data-ttu-id="145bf-133">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-133">Database name.</span></span>

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

### <span data-ttu-id="145bf-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145bf-134">-DefaultProfile</span></span>
<span data-ttu-id="145bf-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145bf-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="145bf-136">-IndexingPolicy</span></span>
<span data-ttu-id="145bf-137">Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="145bf-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="145bf-138">-InputObject</span></span>
<span data-ttu-id="145bf-139">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-139">Sql Container object.</span></span>

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

### <span data-ttu-id="145bf-140">-Name</span><span class="sxs-lookup"><span data-stu-id="145bf-140">-Name</span></span>
<span data-ttu-id="145bf-141">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-141">Container name.</span></span>

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

### <span data-ttu-id="145bf-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="145bf-142">-ParentObject</span></span>
<span data-ttu-id="145bf-143">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-143">Sql Database object.</span></span>

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

### <span data-ttu-id="145bf-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="145bf-144">-PartitionKeyKind</span></span>
<span data-ttu-id="145bf-145">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="145bf-146">가능한 값은 '해시', '범위'입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="145bf-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="145bf-147">-PartitionKeyPath</span></span>
<span data-ttu-id="145bf-148">파티션 키 경로(예: '/address/zipcode')</span><span class="sxs-lookup"><span data-stu-id="145bf-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="145bf-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="145bf-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="145bf-150">파티션 키 정의의 버전</span><span class="sxs-lookup"><span data-stu-id="145bf-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="145bf-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145bf-151">-ResourceGroupName</span></span>
<span data-ttu-id="145bf-152">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-152">Name of resource group.</span></span>

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

### <span data-ttu-id="145bf-153">-Throughput</span><span class="sxs-lookup"><span data-stu-id="145bf-153">-Throughput</span></span>
<span data-ttu-id="145bf-154">컨테이너의 SQL(RU/s)</span><span class="sxs-lookup"><span data-stu-id="145bf-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="145bf-155">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-155">Default value is 400.</span></span>

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

### <span data-ttu-id="145bf-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="145bf-156">-TtlInSeconds</span></span>
<span data-ttu-id="145bf-157">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="145bf-158">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="145bf-159">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="145bf-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="145bf-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="145bf-161">Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="145bf-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145bf-162">-WhatIf</span></span>
<span data-ttu-id="145bf-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="145bf-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145bf-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145bf-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145bf-165">CommonParameters</span></span>
<span data-ttu-id="145bf-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="145bf-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145bf-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="145bf-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145bf-168">입력</span><span class="sxs-lookup"><span data-stu-id="145bf-168">INPUTS</span></span>

### <span data-ttu-id="145bf-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="145bf-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="145bf-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="145bf-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="145bf-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="145bf-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="145bf-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="145bf-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="145bf-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="145bf-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="145bf-174">출력</span><span class="sxs-lookup"><span data-stu-id="145bf-174">OUTPUTS</span></span>

### <span data-ttu-id="145bf-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="145bf-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="145bf-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="145bf-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="145bf-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="145bf-177">NOTES</span></span>

## <span data-ttu-id="145bf-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="145bf-178">RELATED LINKS</span></span>
