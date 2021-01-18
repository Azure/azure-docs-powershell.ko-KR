---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493685"
---
# <span data-ttu-id="f706b-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="f706b-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="f706b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f706b-102">SYNOPSIS</span></span>
<span data-ttu-id="f706b-103">새 CosmosDB Sql 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f706b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f706b-104">SYNTAX</span></span>

### <span data-ttu-id="f706b-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f706b-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f706b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f706b-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f706b-107">설명</span><span class="sxs-lookup"><span data-stu-id="f706b-107">DESCRIPTION</span></span>
<span data-ttu-id="f706b-108">새 CosmosDB Sql 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="f706b-109">예제</span><span class="sxs-lookup"><span data-stu-id="f706b-109">EXAMPLES</span></span>

### <span data-ttu-id="f706b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f706b-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="f706b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f706b-111">PARAMETERS</span></span>

### <span data-ttu-id="f706b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f706b-112">-AccountName</span></span>
<span data-ttu-id="f706b-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f706b-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f706b-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f706b-115">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f706b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f706b-116">-Confirm</span></span>
<span data-ttu-id="f706b-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f706b-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f706b-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f706b-119">제공된 경우 PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체가 컨테이너의 ConflictResolutionPolicy로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f706b-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f706b-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f706b-121">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="f706b-122">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f706b-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f706b-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f706b-124">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="f706b-125">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f706b-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f706b-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f706b-127">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="f706b-128">ConflictResolutionPolicy 매개 변수와 함께 제공된 경우 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="f706b-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f706b-129">-DatabaseName</span></span>
<span data-ttu-id="f706b-130">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-130">Database name.</span></span>

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

### <span data-ttu-id="f706b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f706b-131">-DefaultProfile</span></span>
<span data-ttu-id="f706b-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f706b-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f706b-133">-IndexingPolicy</span></span>
<span data-ttu-id="f706b-134">Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="f706b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="f706b-135">-Name</span></span>
<span data-ttu-id="f706b-136">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-136">Container name.</span></span>

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

### <span data-ttu-id="f706b-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f706b-137">-ParentObject</span></span>
<span data-ttu-id="f706b-138">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-138">Sql Database object.</span></span>

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

### <span data-ttu-id="f706b-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f706b-139">-PartitionKeyKind</span></span>
<span data-ttu-id="f706b-140">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f706b-141">가능한 값은 '해시', '범위'입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f706b-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f706b-142">-PartitionKeyPath</span></span>
<span data-ttu-id="f706b-143">파티션 키 경로(예: '/address/zipcode')</span><span class="sxs-lookup"><span data-stu-id="f706b-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f706b-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f706b-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="f706b-145">파티션 키 정의의 버전</span><span class="sxs-lookup"><span data-stu-id="f706b-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f706b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f706b-146">-ResourceGroupName</span></span>
<span data-ttu-id="f706b-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-147">Name of resource group.</span></span>

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

### <span data-ttu-id="f706b-148">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f706b-148">-Throughput</span></span>
<span data-ttu-id="f706b-149">컨테이너의 SQL(RU/s)</span><span class="sxs-lookup"><span data-stu-id="f706b-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f706b-150">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-150">Default value is 400.</span></span>

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

### <span data-ttu-id="f706b-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f706b-151">-TtlInSeconds</span></span>
<span data-ttu-id="f706b-152">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="f706b-153">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f706b-154">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f706b-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f706b-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f706b-156">Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f706b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f706b-157">-WhatIf</span></span>
<span data-ttu-id="f706b-158">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f706b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f706b-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f706b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f706b-160">CommonParameters</span></span>
<span data-ttu-id="f706b-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f706b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f706b-162">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f706b-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f706b-163">입력</span><span class="sxs-lookup"><span data-stu-id="f706b-163">INPUTS</span></span>

### <span data-ttu-id="f706b-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f706b-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="f706b-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f706b-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="f706b-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f706b-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="f706b-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f706b-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f706b-168">출력</span><span class="sxs-lookup"><span data-stu-id="f706b-168">OUTPUTS</span></span>

### <span data-ttu-id="f706b-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f706b-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f706b-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f706b-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f706b-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f706b-171">NOTES</span></span>

## <span data-ttu-id="f706b-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f706b-172">RELATED LINKS</span></span>
