---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495798"
---
# <span data-ttu-id="c4a24-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="c4a24-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="c4a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a24-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a24-103">새 CosmosDB Gremlin Graph를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c4a24-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4a24-104">SYNTAX</span></span>

### <span data-ttu-id="c4a24-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4a24-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a24-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a24-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4a24-107">설명</span><span class="sxs-lookup"><span data-stu-id="c4a24-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a24-108">새 CosmosDB Gremlin Graph를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="c4a24-109">예제</span><span class="sxs-lookup"><span data-stu-id="c4a24-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a24-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4a24-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="c4a24-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4a24-111">PARAMETERS</span></span>

### <span data-ttu-id="c4a24-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4a24-112">-AccountName</span></span>
<span data-ttu-id="c4a24-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c4a24-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c4a24-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c4a24-115">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c4a24-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4a24-116">-Confirm</span></span>
<span data-ttu-id="c4a24-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a24-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a24-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c4a24-119">제공된 경우 PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체가 컨테이너의 ConflictResolutionPolicy로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="c4a24-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="c4a24-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="c4a24-121">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="c4a24-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="c4a24-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="c4a24-123">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="c4a24-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="c4a24-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="c4a24-125">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="c4a24-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4a24-126">-DatabaseName</span></span>
<span data-ttu-id="c4a24-127">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-127">Database name.</span></span>

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

### <span data-ttu-id="c4a24-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a24-128">-DefaultProfile</span></span>
<span data-ttu-id="c4a24-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a24-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a24-130">-IndexingPolicy</span></span>
<span data-ttu-id="c4a24-131">Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="c4a24-132">-Name</span><span class="sxs-lookup"><span data-stu-id="c4a24-132">-Name</span></span>
<span data-ttu-id="c4a24-133">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="c4a24-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c4a24-134">-ParentObject</span></span>
<span data-ttu-id="c4a24-135">Gremlin 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="c4a24-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="c4a24-136">-PartitionKeyKind</span></span>
<span data-ttu-id="c4a24-137">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="c4a24-138">가능한 값은 '해시', '범위'입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="c4a24-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="c4a24-139">-PartitionKeyPath</span></span>
<span data-ttu-id="c4a24-140">파티션 키 경로(예: '/address/zipcode')</span><span class="sxs-lookup"><span data-stu-id="c4a24-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="c4a24-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="c4a24-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="c4a24-142">파티션 키 정의의 버전</span><span class="sxs-lookup"><span data-stu-id="c4a24-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="c4a24-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a24-143">-ResourceGroupName</span></span>
<span data-ttu-id="c4a24-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-144">Name of resource group.</span></span>

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

### <span data-ttu-id="c4a24-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="c4a24-145">-Throughput</span></span>
<span data-ttu-id="c4a24-146">Gremlin Graph(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="c4a24-147">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-147">Default value is 400.</span></span>

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

### <span data-ttu-id="c4a24-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="c4a24-148">-TtlInSeconds</span></span>
<span data-ttu-id="c4a24-149">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="c4a24-150">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="c4a24-151">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="c4a24-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a24-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="c4a24-153">Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="c4a24-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a24-154">-WhatIf</span></span>
<span data-ttu-id="c4a24-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4a24-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a24-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a24-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a24-157">CommonParameters</span></span>
<span data-ttu-id="c4a24-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a24-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a24-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4a24-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a24-160">입력</span><span class="sxs-lookup"><span data-stu-id="c4a24-160">INPUTS</span></span>

### <span data-ttu-id="c4a24-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a24-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="c4a24-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a24-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="c4a24-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c4a24-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="c4a24-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c4a24-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="c4a24-165">출력</span><span class="sxs-lookup"><span data-stu-id="c4a24-165">OUTPUTS</span></span>

### <span data-ttu-id="c4a24-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="c4a24-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="c4a24-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c4a24-167">System.Exception</span></span>

## <span data-ttu-id="c4a24-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4a24-168">NOTES</span></span>

## <span data-ttu-id="c4a24-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4a24-169">RELATED LINKS</span></span>
