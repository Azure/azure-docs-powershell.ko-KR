---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306803"
---
# <span data-ttu-id="25cd9-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="25cd9-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="25cd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="25cd9-103">CosmosDB Gremlin 그래프를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="25cd9-104">기존 그래프를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="25cd9-105">구문과</span><span class="sxs-lookup"><span data-stu-id="25cd9-105">SYNTAX</span></span>

### <span data-ttu-id="25cd9-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="25cd9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cd9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cd9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cd9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25cd9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25cd9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="25cd9-109">DESCRIPTION</span></span>
<span data-ttu-id="25cd9-110">CosmosDB Gremlin 그래프를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="25cd9-111">기존 그래프를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="25cd9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="25cd9-112">EXAMPLES</span></span>

### <span data-ttu-id="25cd9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="25cd9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="25cd9-114">변수</span><span class="sxs-lookup"><span data-stu-id="25cd9-114">PARAMETERS</span></span>

### <span data-ttu-id="25cd9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25cd9-115">-AccountName</span></span>
<span data-ttu-id="25cd9-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="25cd9-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="25cd9-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="25cd9-118">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="25cd9-119">-확인</span><span class="sxs-lookup"><span data-stu-id="25cd9-119">-Confirm</span></span>
<span data-ttu-id="25cd9-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25cd9-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="25cd9-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="25cd9-122">PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 제공 되는 경우 컨테이너의 ConflictResolutionPolicy로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="25cd9-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="25cd9-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="25cd9-124">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="25cd9-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="25cd9-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="25cd9-126">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="25cd9-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="25cd9-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="25cd9-128">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="25cd9-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25cd9-129">-DatabaseName</span></span>
<span data-ttu-id="25cd9-130">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-130">Database name.</span></span>

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

### <span data-ttu-id="25cd9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cd9-131">-DefaultProfile</span></span>
<span data-ttu-id="25cd9-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25cd9-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="25cd9-133">-IndexingPolicy</span></span>
<span data-ttu-id="25cd9-134">CosmosDB Indexingpolicy 유형의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="25cd9-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25cd9-135">-InputObject</span></span>
<span data-ttu-id="25cd9-136">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="25cd9-137">-이름</span><span class="sxs-lookup"><span data-stu-id="25cd9-137">-Name</span></span>
<span data-ttu-id="25cd9-138">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="25cd9-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="25cd9-139">-ParentObject</span></span>
<span data-ttu-id="25cd9-140">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="25cd9-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="25cd9-141">-파티션 형식</span><span class="sxs-lookup"><span data-stu-id="25cd9-141">-PartitionKeyKind</span></span>
<span data-ttu-id="25cd9-142">분할에 사용 되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="25cd9-143">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="25cd9-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="25cd9-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="25cd9-144">-PartitionKeyPath</span></span>
<span data-ttu-id="25cd9-145">파티션 키 경로 (예: '/address/zipcode ').</span><span class="sxs-lookup"><span data-stu-id="25cd9-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="25cd9-146">-파티션 버전</span><span class="sxs-lookup"><span data-stu-id="25cd9-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="25cd9-147">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="25cd9-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="25cd9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25cd9-148">-ResourceGroupName</span></span>
<span data-ttu-id="25cd9-149">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-149">Name of resource group.</span></span>

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

### <span data-ttu-id="25cd9-150">-처리량</span><span class="sxs-lookup"><span data-stu-id="25cd9-150">-Throughput</span></span>
<span data-ttu-id="25cd9-151">Gremlin 그래프의 처리량 (1/s)</span><span class="sxs-lookup"><span data-stu-id="25cd9-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="25cd9-152">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-152">Default value is 400.</span></span>

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

### <span data-ttu-id="25cd9-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="25cd9-153">-TtlInSeconds</span></span>
<span data-ttu-id="25cd9-154">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="25cd9-155">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="25cd9-156">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="25cd9-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="25cd9-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="25cd9-158">UniqueKeyPolicy. CosmosDB. PSUniqueKeyPolicy의 형식 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="25cd9-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25cd9-159">-WhatIf</span></span>
<span data-ttu-id="25cd9-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25cd9-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25cd9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cd9-162">CommonParameters</span></span>
<span data-ttu-id="25cd9-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25cd9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cd9-164">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="25cd9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cd9-165">입력</span><span class="sxs-lookup"><span data-stu-id="25cd9-165">INPUTS</span></span>

### <span data-ttu-id="25cd9-166">CosmosDB. a m a. m 인덱스 Ingpolicy</span><span class="sxs-lookup"><span data-stu-id="25cd9-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="25cd9-167">CosmosDB. PSUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="25cd9-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="25cd9-168">CosmosDB. PSConflictResolutionPolicy/.</span><span class="sxs-lookup"><span data-stu-id="25cd9-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="25cd9-169">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="25cd9-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="25cd9-170">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="25cd9-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="25cd9-171">출력</span><span class="sxs-lookup"><span data-stu-id="25cd9-171">OUTPUTS</span></span>

### <span data-ttu-id="25cd9-172">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="25cd9-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="25cd9-173">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="25cd9-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="25cd9-174">상속자</span><span class="sxs-lookup"><span data-stu-id="25cd9-174">NOTES</span></span>

## <span data-ttu-id="25cd9-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25cd9-175">RELATED LINKS</span></span>
