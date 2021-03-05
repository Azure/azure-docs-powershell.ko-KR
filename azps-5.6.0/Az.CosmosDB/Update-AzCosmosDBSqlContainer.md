---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: a36222b3a6cacf567fd0b5e7541c2dc53a44fa22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977264"
---
# <span data-ttu-id="02f64-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="02f64-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="02f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f64-102">SYNOPSIS</span></span>
<span data-ttu-id="02f64-103">CosmosDB Sql Container를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="02f64-104">기존 컨테이너를 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="02f64-105">구문</span><span class="sxs-lookup"><span data-stu-id="02f64-105">SYNTAX</span></span>

### <span data-ttu-id="02f64-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="02f64-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02f64-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f64-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02f64-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f64-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02f64-109">설명</span><span class="sxs-lookup"><span data-stu-id="02f64-109">DESCRIPTION</span></span>
<span data-ttu-id="02f64-110">CosmosDB Sql Container를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="02f64-111">기존 컨테이너를 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="02f64-112">예제</span><span class="sxs-lookup"><span data-stu-id="02f64-112">EXAMPLES</span></span>

### <span data-ttu-id="02f64-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="02f64-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="02f64-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="02f64-114">PARAMETERS</span></span>

### <span data-ttu-id="02f64-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02f64-115">-AccountName</span></span>
<span data-ttu-id="02f64-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02f64-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="02f64-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="02f64-118">분석 저장소용 TTL(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="02f64-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="02f64-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="02f64-120">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="02f64-121">-확인</span><span class="sxs-lookup"><span data-stu-id="02f64-121">-Confirm</span></span>
<span data-ttu-id="02f64-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f64-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="02f64-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="02f64-124">이 개체가 컨테이너의 ConflictResolutionPolicy로 설정되어 있는 경우 PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="02f64-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="02f64-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="02f64-126">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="02f64-127">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="02f64-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="02f64-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="02f64-129">형식이 LastWriterWins일 때 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="02f64-130">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="02f64-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="02f64-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="02f64-132">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="02f64-133">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="02f64-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02f64-134">-DatabaseName</span></span>
<span data-ttu-id="02f64-135">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-135">Database name.</span></span>

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

### <span data-ttu-id="02f64-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f64-136">-DefaultProfile</span></span>
<span data-ttu-id="02f64-137">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02f64-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="02f64-138">-IndexingPolicy</span></span>
<span data-ttu-id="02f64-139">Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="02f64-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02f64-140">-InputObject</span></span>
<span data-ttu-id="02f64-141">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-141">Sql Container object.</span></span>

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

### <span data-ttu-id="02f64-142">-Name</span><span class="sxs-lookup"><span data-stu-id="02f64-142">-Name</span></span>
<span data-ttu-id="02f64-143">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-143">Container name.</span></span>

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

### <span data-ttu-id="02f64-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02f64-144">-ParentObject</span></span>
<span data-ttu-id="02f64-145">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-145">Sql Database object.</span></span>

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

### <span data-ttu-id="02f64-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="02f64-146">-PartitionKeyKind</span></span>
<span data-ttu-id="02f64-147">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="02f64-148">가능한 값은 다음과 같습니다. '해시', '범위'</span><span class="sxs-lookup"><span data-stu-id="02f64-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="02f64-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="02f64-149">-PartitionKeyPath</span></span>
<span data-ttu-id="02f64-150">파티션 키 경로(예: '/address/zipcode').</span><span class="sxs-lookup"><span data-stu-id="02f64-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="02f64-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="02f64-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="02f64-152">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="02f64-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="02f64-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f64-153">-ResourceGroupName</span></span>
<span data-ttu-id="02f64-154">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-154">Name of resource group.</span></span>

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

### <span data-ttu-id="02f64-155">-Throughput</span><span class="sxs-lookup"><span data-stu-id="02f64-155">-Throughput</span></span>
<span data-ttu-id="02f64-156">RU/s SQL 컨테이너의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="02f64-157">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-157">Default value is 400.</span></span>

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

### <span data-ttu-id="02f64-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="02f64-158">-TtlInSeconds</span></span>
<span data-ttu-id="02f64-159">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="02f64-160">값이 누락되거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="02f64-161">값이 n으로 설정되어 있는 경우 항목은 마지막 수정된 시간 후에 n초가 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="02f64-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="02f64-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="02f64-163">Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="02f64-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f64-164">-WhatIf</span></span>
<span data-ttu-id="02f64-165">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f64-166">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f64-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f64-167">CommonParameters</span></span>
<span data-ttu-id="02f64-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02f64-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f64-169">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02f64-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f64-170">입력</span><span class="sxs-lookup"><span data-stu-id="02f64-170">INPUTS</span></span>

### <span data-ttu-id="02f64-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="02f64-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="02f64-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="02f64-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="02f64-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="02f64-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="02f64-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="02f64-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="02f64-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="02f64-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="02f64-176">출력</span><span class="sxs-lookup"><span data-stu-id="02f64-176">OUTPUTS</span></span>

### <span data-ttu-id="02f64-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="02f64-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="02f64-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="02f64-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="02f64-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02f64-179">NOTES</span></span>

## <span data-ttu-id="02f64-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02f64-180">RELATED LINKS</span></span>
