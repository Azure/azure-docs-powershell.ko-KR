---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329370"
---
# <span data-ttu-id="37529-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="37529-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="37529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37529-102">SYNOPSIS</span></span>
<span data-ttu-id="37529-103">CosmosDB Gremlin Graph를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="37529-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="37529-104">기존 Graph를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="37529-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="37529-105">구문</span><span class="sxs-lookup"><span data-stu-id="37529-105">SYNTAX</span></span>

### <span data-ttu-id="37529-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="37529-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37529-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37529-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37529-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37529-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37529-109">설명</span><span class="sxs-lookup"><span data-stu-id="37529-109">DESCRIPTION</span></span>
<span data-ttu-id="37529-110">CosmosDB Gremlin Graph를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="37529-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="37529-111">기존 Graph를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="37529-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="37529-112">예제</span><span class="sxs-lookup"><span data-stu-id="37529-112">EXAMPLES</span></span>

### <span data-ttu-id="37529-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="37529-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="37529-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37529-114">PARAMETERS</span></span>

### <span data-ttu-id="37529-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="37529-115">-AccountName</span></span>
<span data-ttu-id="37529-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="37529-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="37529-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="37529-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="37529-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37529-119">-Confirm</span></span>
<span data-ttu-id="37529-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37529-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37529-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="37529-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="37529-122">제공된 경우 PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체가 컨테이너의 ConflictResolutionPolicy로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="37529-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="37529-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="37529-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="37529-124">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37529-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="37529-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="37529-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="37529-126">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37529-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="37529-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="37529-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="37529-128">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37529-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="37529-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37529-129">-DatabaseName</span></span>
<span data-ttu-id="37529-130">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-130">Database name.</span></span>

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

### <span data-ttu-id="37529-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37529-131">-DefaultProfile</span></span>
<span data-ttu-id="37529-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37529-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="37529-133">-IndexingPolicy</span></span>
<span data-ttu-id="37529-134">Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="37529-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37529-135">-InputObject</span></span>
<span data-ttu-id="37529-136">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="37529-137">-Name</span><span class="sxs-lookup"><span data-stu-id="37529-137">-Name</span></span>
<span data-ttu-id="37529-138">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="37529-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37529-139">-ParentObject</span></span>
<span data-ttu-id="37529-140">Gremlin 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="37529-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="37529-141">-PartitionKeyKind</span></span>
<span data-ttu-id="37529-142">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="37529-143">가능한 값은 '해시', '범위'입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="37529-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="37529-144">-PartitionKeyPath</span></span>
<span data-ttu-id="37529-145">파티션 키 경로(예: '/address/zipcode')</span><span class="sxs-lookup"><span data-stu-id="37529-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="37529-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="37529-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="37529-147">파티션 키 정의의 버전</span><span class="sxs-lookup"><span data-stu-id="37529-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="37529-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37529-148">-ResourceGroupName</span></span>
<span data-ttu-id="37529-149">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-149">Name of resource group.</span></span>

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

### <span data-ttu-id="37529-150">-Throughput</span><span class="sxs-lookup"><span data-stu-id="37529-150">-Throughput</span></span>
<span data-ttu-id="37529-151">Gremlin Graph(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="37529-152">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-152">Default value is 400.</span></span>

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

### <span data-ttu-id="37529-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="37529-153">-TtlInSeconds</span></span>
<span data-ttu-id="37529-154">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="37529-155">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37529-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="37529-156">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="37529-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="37529-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="37529-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="37529-158">Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37529-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="37529-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37529-159">-WhatIf</span></span>
<span data-ttu-id="37529-160">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37529-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37529-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37529-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37529-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37529-162">CommonParameters</span></span>
<span data-ttu-id="37529-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37529-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37529-164">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37529-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37529-165">입력</span><span class="sxs-lookup"><span data-stu-id="37529-165">INPUTS</span></span>

### <span data-ttu-id="37529-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="37529-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="37529-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="37529-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="37529-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="37529-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="37529-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="37529-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="37529-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="37529-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="37529-171">출력</span><span class="sxs-lookup"><span data-stu-id="37529-171">OUTPUTS</span></span>

### <span data-ttu-id="37529-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="37529-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="37529-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="37529-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="37529-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37529-174">NOTES</span></span>

## <span data-ttu-id="37529-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37529-175">RELATED LINKS</span></span>
