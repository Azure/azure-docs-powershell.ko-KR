---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 4fc4bd816511132d5a4fd5d317069e3baf9d9225
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966688"
---
# <span data-ttu-id="15060-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="15060-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="15060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15060-102">SYNOPSIS</span></span>
<span data-ttu-id="15060-103">새 CosmosDB Sql Container를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15060-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="15060-104">구문</span><span class="sxs-lookup"><span data-stu-id="15060-104">SYNTAX</span></span>

### <span data-ttu-id="15060-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="15060-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15060-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15060-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15060-107">설명</span><span class="sxs-lookup"><span data-stu-id="15060-107">DESCRIPTION</span></span>
<span data-ttu-id="15060-108">새 CosmosDB Sql Container를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15060-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="15060-109">예제</span><span class="sxs-lookup"><span data-stu-id="15060-109">EXAMPLES</span></span>

### <span data-ttu-id="15060-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="15060-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="15060-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15060-111">PARAMETERS</span></span>

### <span data-ttu-id="15060-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15060-112">-AccountName</span></span>
<span data-ttu-id="15060-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="15060-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="15060-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="15060-115">분석 저장소용 TTL(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="15060-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="15060-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="15060-117">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="15060-118">-확인</span><span class="sxs-lookup"><span data-stu-id="15060-118">-Confirm</span></span>
<span data-ttu-id="15060-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15060-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15060-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="15060-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="15060-121">이 개체가 컨테이너의 ConflictResolutionPolicy로 설정되어 있는 경우 PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="15060-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="15060-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="15060-123">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15060-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="15060-124">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15060-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="15060-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="15060-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="15060-126">형식이 LastWriterWins일 때 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="15060-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="15060-127">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15060-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="15060-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="15060-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="15060-129">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15060-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="15060-130">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15060-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="15060-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15060-131">-DatabaseName</span></span>
<span data-ttu-id="15060-132">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-132">Database name.</span></span>

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

### <span data-ttu-id="15060-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15060-133">-DefaultProfile</span></span>
<span data-ttu-id="15060-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15060-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="15060-135">-IndexingPolicy</span></span>
<span data-ttu-id="15060-136">Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="15060-137">-Name</span><span class="sxs-lookup"><span data-stu-id="15060-137">-Name</span></span>
<span data-ttu-id="15060-138">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-138">Container name.</span></span>

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

### <span data-ttu-id="15060-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15060-139">-ParentObject</span></span>
<span data-ttu-id="15060-140">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-140">Sql Database object.</span></span>

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

### <span data-ttu-id="15060-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="15060-141">-PartitionKeyKind</span></span>
<span data-ttu-id="15060-142">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="15060-143">가능한 값은 다음과 같습니다. '해시', '범위'</span><span class="sxs-lookup"><span data-stu-id="15060-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="15060-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="15060-144">-PartitionKeyPath</span></span>
<span data-ttu-id="15060-145">파티션 키 경로(예: '/address/zipcode').</span><span class="sxs-lookup"><span data-stu-id="15060-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="15060-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="15060-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="15060-147">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="15060-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="15060-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15060-148">-ResourceGroupName</span></span>
<span data-ttu-id="15060-149">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-149">Name of resource group.</span></span>

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

### <span data-ttu-id="15060-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="15060-150">-Throughput</span></span>
<span data-ttu-id="15060-151">RU/s SQL 컨테이너의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="15060-152">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-152">Default value is 400.</span></span>

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

### <span data-ttu-id="15060-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="15060-153">-TtlInSeconds</span></span>
<span data-ttu-id="15060-154">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="15060-155">값이 누락되거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15060-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="15060-156">값이 n으로 설정되어 있는 경우 항목은 마지막 수정된 시간 후에 n초가 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="15060-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="15060-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="15060-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="15060-158">Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15060-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="15060-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15060-159">-WhatIf</span></span>
<span data-ttu-id="15060-160">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="15060-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15060-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15060-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15060-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15060-162">CommonParameters</span></span>
<span data-ttu-id="15060-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15060-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15060-164">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15060-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15060-165">입력</span><span class="sxs-lookup"><span data-stu-id="15060-165">INPUTS</span></span>

### <span data-ttu-id="15060-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="15060-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="15060-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="15060-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="15060-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="15060-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="15060-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="15060-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="15060-170">출력</span><span class="sxs-lookup"><span data-stu-id="15060-170">OUTPUTS</span></span>

### <span data-ttu-id="15060-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="15060-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="15060-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="15060-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="15060-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15060-173">NOTES</span></span>

## <span data-ttu-id="15060-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15060-174">RELATED LINKS</span></span>
