---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196828"
---
# <span data-ttu-id="f9dce-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="f9dce-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="f9dce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9dce-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dce-103">새 CosmosDB Gremlin Graph를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f9dce-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9dce-104">SYNTAX</span></span>

### <span data-ttu-id="f9dce-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9dce-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9dce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dce-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9dce-107">설명</span><span class="sxs-lookup"><span data-stu-id="f9dce-107">DESCRIPTION</span></span>
<span data-ttu-id="f9dce-108">새 CosmosDB Gremlin Graph를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f9dce-109">예제</span><span class="sxs-lookup"><span data-stu-id="f9dce-109">EXAMPLES</span></span>

### <span data-ttu-id="f9dce-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9dce-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="f9dce-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9dce-111">PARAMETERS</span></span>

### <span data-ttu-id="f9dce-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f9dce-112">-AccountName</span></span>
<span data-ttu-id="f9dce-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f9dce-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f9dce-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f9dce-115">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f9dce-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9dce-116">-Confirm</span></span>
<span data-ttu-id="f9dce-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9dce-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dce-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="f9dce-119">제공된 경우 PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 컨테이너의 ConflictResolutionPolicy로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="f9dce-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="f9dce-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="f9dce-121">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="f9dce-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="f9dce-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="f9dce-123">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="f9dce-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="f9dce-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="f9dce-125">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="f9dce-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9dce-126">-DatabaseName</span></span>
<span data-ttu-id="f9dce-127">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-127">Database name.</span></span>

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

### <span data-ttu-id="f9dce-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dce-128">-DefaultProfile</span></span>
<span data-ttu-id="f9dce-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9dce-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dce-130">-IndexingPolicy</span></span>
<span data-ttu-id="f9dce-131">Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy 형식의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="f9dce-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f9dce-132">-Name</span></span>
<span data-ttu-id="f9dce-133">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f9dce-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f9dce-134">-ParentObject</span></span>
<span data-ttu-id="f9dce-135">Gremlin 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="f9dce-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="f9dce-136">-PartitionKeyKind</span></span>
<span data-ttu-id="f9dce-137">분할에 사용되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="f9dce-138">가능한 값은 '해시', '범위'입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="f9dce-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="f9dce-139">-PartitionKeyPath</span></span>
<span data-ttu-id="f9dce-140">파티션 키 경로(예: '/address/zipcode')</span><span class="sxs-lookup"><span data-stu-id="f9dce-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="f9dce-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f9dce-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="f9dce-142">파티션 키 정의의 버전</span><span class="sxs-lookup"><span data-stu-id="f9dce-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="f9dce-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dce-143">-ResourceGroupName</span></span>
<span data-ttu-id="f9dce-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-144">Name of resource group.</span></span>

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

### <span data-ttu-id="f9dce-145">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f9dce-145">-Throughput</span></span>
<span data-ttu-id="f9dce-146">Gremlin Graph(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f9dce-147">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-147">Default value is 400.</span></span>

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

### <span data-ttu-id="f9dce-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f9dce-148">-TtlInSeconds</span></span>
<span data-ttu-id="f9dce-149">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="f9dce-150">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="f9dce-151">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="f9dce-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dce-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="f9dce-153">Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy 형식의 UniqueKeyPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="f9dce-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9dce-154">-WhatIf</span></span>
<span data-ttu-id="f9dce-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f9dce-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9dce-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9dce-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dce-157">CommonParameters</span></span>
<span data-ttu-id="f9dce-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9dce-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dce-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9dce-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dce-160">입력</span><span class="sxs-lookup"><span data-stu-id="f9dce-160">INPUTS</span></span>

### <span data-ttu-id="f9dce-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dce-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="f9dce-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dce-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="f9dce-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="f9dce-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="f9dce-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f9dce-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f9dce-165">출력</span><span class="sxs-lookup"><span data-stu-id="f9dce-165">OUTPUTS</span></span>

### <span data-ttu-id="f9dce-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="f9dce-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="f9dce-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f9dce-167">System.Exception</span></span>

## <span data-ttu-id="f9dce-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9dce-168">NOTES</span></span>

## <span data-ttu-id="f9dce-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9dce-169">RELATED LINKS</span></span>
