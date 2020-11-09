---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307088"
---
# <span data-ttu-id="e559f-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="e559f-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="e559f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e559f-102">SYNOPSIS</span></span>
<span data-ttu-id="e559f-103">새 CosmosDB Gremlin 그래프를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="e559f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e559f-104">SYNTAX</span></span>

### <span data-ttu-id="e559f-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e559f-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e559f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e559f-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e559f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e559f-107">DESCRIPTION</span></span>
<span data-ttu-id="e559f-108">새 CosmosDB Gremlin 그래프를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="e559f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e559f-109">EXAMPLES</span></span>

### <span data-ttu-id="e559f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e559f-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="e559f-111">변수</span><span class="sxs-lookup"><span data-stu-id="e559f-111">PARAMETERS</span></span>

### <span data-ttu-id="e559f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e559f-112">-AccountName</span></span>
<span data-ttu-id="e559f-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e559f-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e559f-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e559f-115">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e559f-116">-확인</span><span class="sxs-lookup"><span data-stu-id="e559f-116">-Confirm</span></span>
<span data-ttu-id="e559f-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e559f-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e559f-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e559f-119">PSConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 제공 되는 경우 컨테이너의 ConflictResolutionPolicy로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="e559f-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="e559f-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="e559f-121">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="e559f-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="e559f-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="e559f-123">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="e559f-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="e559f-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="e559f-125">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="e559f-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e559f-126">-DatabaseName</span></span>
<span data-ttu-id="e559f-127">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-127">Database name.</span></span>

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

### <span data-ttu-id="e559f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e559f-128">-DefaultProfile</span></span>
<span data-ttu-id="e559f-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e559f-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e559f-130">-IndexingPolicy</span></span>
<span data-ttu-id="e559f-131">CosmosDB Indexingpolicy 유형의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="e559f-132">-이름</span><span class="sxs-lookup"><span data-stu-id="e559f-132">-Name</span></span>
<span data-ttu-id="e559f-133">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="e559f-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e559f-134">-ParentObject</span></span>
<span data-ttu-id="e559f-135">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="e559f-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="e559f-136">-파티션 형식</span><span class="sxs-lookup"><span data-stu-id="e559f-136">-PartitionKeyKind</span></span>
<span data-ttu-id="e559f-137">분할에 사용 되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="e559f-138">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="e559f-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="e559f-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="e559f-139">-PartitionKeyPath</span></span>
<span data-ttu-id="e559f-140">파티션 키 경로 (예: '/address/zipcode ').</span><span class="sxs-lookup"><span data-stu-id="e559f-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="e559f-141">-파티션 버전</span><span class="sxs-lookup"><span data-stu-id="e559f-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="e559f-142">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="e559f-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="e559f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e559f-143">-ResourceGroupName</span></span>
<span data-ttu-id="e559f-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-144">Name of resource group.</span></span>

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

### <span data-ttu-id="e559f-145">-처리량</span><span class="sxs-lookup"><span data-stu-id="e559f-145">-Throughput</span></span>
<span data-ttu-id="e559f-146">Gremlin 그래프의 처리량 (1/s)</span><span class="sxs-lookup"><span data-stu-id="e559f-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="e559f-147">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-147">Default value is 400.</span></span>

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

### <span data-ttu-id="e559f-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e559f-148">-TtlInSeconds</span></span>
<span data-ttu-id="e559f-149">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="e559f-150">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="e559f-151">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="e559f-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e559f-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="e559f-153">UniqueKeyPolicy. CosmosDB. PSUniqueKeyPolicy의 형식 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="e559f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e559f-154">-WhatIf</span></span>
<span data-ttu-id="e559f-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e559f-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e559f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e559f-157">CommonParameters</span></span>
<span data-ttu-id="e559f-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e559f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e559f-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e559f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e559f-160">입력</span><span class="sxs-lookup"><span data-stu-id="e559f-160">INPUTS</span></span>

### <span data-ttu-id="e559f-161">CosmosDB. a m a. m 인덱스 Ingpolicy</span><span class="sxs-lookup"><span data-stu-id="e559f-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="e559f-162">CosmosDB. PSUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="e559f-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="e559f-163">CosmosDB. PSConflictResolutionPolicy/.</span><span class="sxs-lookup"><span data-stu-id="e559f-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="e559f-164">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="e559f-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="e559f-165">출력</span><span class="sxs-lookup"><span data-stu-id="e559f-165">OUTPUTS</span></span>

### <span data-ttu-id="e559f-166">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="e559f-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="e559f-167">시스템. 예외</span><span class="sxs-lookup"><span data-stu-id="e559f-167">System.Exception</span></span>

## <span data-ttu-id="e559f-168">상속자</span><span class="sxs-lookup"><span data-stu-id="e559f-168">NOTES</span></span>

## <span data-ttu-id="e559f-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e559f-169">RELATED LINKS</span></span>
