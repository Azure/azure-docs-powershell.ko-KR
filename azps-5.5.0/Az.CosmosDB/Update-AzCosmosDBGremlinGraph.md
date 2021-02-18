---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181265"
---
# <span data-ttu-id="d5d84-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="d5d84-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="d5d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d84-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d84-103">CosmosDB Gremlin Graph를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="d5d84-104">기존 Graph를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="d5d84-105">구문</span><span class="sxs-lookup"><span data-stu-id="d5d84-105">SYNTAX</span></span>

### <span data-ttu-id="d5d84-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d5d84-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d84-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d84-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5d84-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d84-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d84-109">설명</span><span class="sxs-lookup"><span data-stu-id="d5d84-109">DESCRIPTION</span></span>
<span data-ttu-id="d5d84-110">CosmosDB Gremlin Graph를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="d5d84-111">기존 Graph를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="d5d84-112">예제</span><span class="sxs-lookup"><span data-stu-id="d5d84-112">EXAMPLES</span></span>

### <span data-ttu-id="d5d84-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5d84-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="d5d84-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5d84-114">PARAMETERS</span></span>

### <span data-ttu-id="d5d84-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d5d84-115">-AccountName</span></span>
<span data-ttu-id="d5d84-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d5d84-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d5d84-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d5d84-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d5d84-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5d84-119">-Confirm</span></span>
<span data-ttu-id="d5d84-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d84-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d84-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="d5d84-122">제공된 경우 PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체가 컨테이너의 ConflictResolutionPolicy로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="d5d84-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d5d84-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="d5d84-124">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="d5d84-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="d5d84-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="d5d84-126">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="d5d84-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="d5d84-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="d5d84-128">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="d5d84-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5d84-129">-DatabaseName</span></span>
<span data-ttu-id="d5d84-130">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-130">Database name.</span></span>

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

### <span data-ttu-id="d5d84-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d84-131">-DefaultProfile</span></span>
<span data-ttu-id="d5d84-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d84-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d84-133">-IndexingPolicy</span></span>
<span data-ttu-id="d5d84-134">Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="d5d84-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5d84-135">-InputObject</span></span>
<span data-ttu-id="d5d84-136">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d84-137">-Name</span><span class="sxs-lookup"><span data-stu-id="d5d84-137">-Name</span></span>
<span data-ttu-id="d5d84-138">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d5d84-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d5d84-139">-ParentObject</span></span>
<span data-ttu-id="d5d84-140">Gremlin 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d5d84-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="d5d84-141">-PartitionKeyKind</span></span>
<span data-ttu-id="d5d84-142">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="d5d84-143">가능한 값은 '해시', '범위'입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="d5d84-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="d5d84-144">-PartitionKeyPath</span></span>
<span data-ttu-id="d5d84-145">파티션 키 경로(예: '/address/zipcode')</span><span class="sxs-lookup"><span data-stu-id="d5d84-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="d5d84-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d5d84-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="d5d84-147">파티션 키 정의의 버전</span><span class="sxs-lookup"><span data-stu-id="d5d84-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="d5d84-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d84-148">-ResourceGroupName</span></span>
<span data-ttu-id="d5d84-149">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-149">Name of resource group.</span></span>

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

### <span data-ttu-id="d5d84-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d5d84-150">-Throughput</span></span>
<span data-ttu-id="d5d84-151">Gremlin Graph(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="d5d84-152">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-152">Default value is 400.</span></span>

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

### <span data-ttu-id="d5d84-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5d84-153">-TtlInSeconds</span></span>
<span data-ttu-id="d5d84-154">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="d5d84-155">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="d5d84-156">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="d5d84-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d84-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="d5d84-158">Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="d5d84-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d84-159">-WhatIf</span></span>
<span data-ttu-id="d5d84-160">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d5d84-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5d84-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d84-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d84-162">CommonParameters</span></span>
<span data-ttu-id="d5d84-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5d84-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d84-164">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5d84-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d84-165">입력</span><span class="sxs-lookup"><span data-stu-id="d5d84-165">INPUTS</span></span>

### <span data-ttu-id="d5d84-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d84-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="d5d84-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d84-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="d5d84-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d84-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="d5d84-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d5d84-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="d5d84-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d5d84-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="d5d84-171">출력</span><span class="sxs-lookup"><span data-stu-id="d5d84-171">OUTPUTS</span></span>

### <span data-ttu-id="d5d84-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d5d84-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="d5d84-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d5d84-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d5d84-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5d84-174">NOTES</span></span>

## <span data-ttu-id="d5d84-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5d84-175">RELATED LINKS</span></span>
