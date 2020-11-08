---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044425"
---
# <span data-ttu-id="547da-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="547da-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="547da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="547da-102">SYNOPSIS</span></span>
<span data-ttu-id="547da-103">기존 CosmosDB Sql 컨테이너를 새로 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="547da-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="547da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="547da-104">SYNTAX</span></span>

### <span data-ttu-id="547da-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="547da-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="547da-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="547da-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="547da-107">설명은</span><span class="sxs-lookup"><span data-stu-id="547da-107">DESCRIPTION</span></span>
<span data-ttu-id="547da-108">**AzCosmosDBSqlContainer** cmdlet은 새 CosmosDB Sql 컨테이너를 새로 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="547da-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="547da-109">예제의</span><span class="sxs-lookup"><span data-stu-id="547da-109">EXAMPLES</span></span>

### <span data-ttu-id="547da-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="547da-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="547da-111">변수</span><span class="sxs-lookup"><span data-stu-id="547da-111">PARAMETERS</span></span>

### <span data-ttu-id="547da-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="547da-112">-AccountName</span></span>
<span data-ttu-id="547da-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="547da-114">-확인</span><span class="sxs-lookup"><span data-stu-id="547da-114">-Confirm</span></span>
<span data-ttu-id="547da-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="547da-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="547da-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="547da-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="547da-117">PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 제공 되는 경우 컨테이너의 ConflictResolutionPolicy로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="547da-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="547da-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="547da-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="547da-119">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="547da-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="547da-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="547da-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="547da-121">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="547da-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="547da-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="547da-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="547da-123">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="547da-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="547da-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="547da-124">-DatabaseName</span></span>
<span data-ttu-id="547da-125">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-125">Database name.</span></span>

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

### <span data-ttu-id="547da-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547da-126">-DefaultProfile</span></span>
<span data-ttu-id="547da-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="547da-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="547da-128">-IndexingPolicy</span></span>
<span data-ttu-id="547da-129">CosmosDB Sqlindexingpolicy 유형의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="547da-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="547da-130">-InputObject</span></span>
<span data-ttu-id="547da-131">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="547da-131">Sql Database object.</span></span>

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

### <span data-ttu-id="547da-132">-이름</span><span class="sxs-lookup"><span data-stu-id="547da-132">-Name</span></span>
<span data-ttu-id="547da-133">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-133">Container name.</span></span>

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

### <span data-ttu-id="547da-134">-파티션 형식</span><span class="sxs-lookup"><span data-stu-id="547da-134">-PartitionKeyKind</span></span>
<span data-ttu-id="547da-135">분할에 사용 되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="547da-136">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="547da-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="547da-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="547da-137">-PartitionKeyPath</span></span>
<span data-ttu-id="547da-138">파티션 키 경로 (예: '/address/zipcode ').</span><span class="sxs-lookup"><span data-stu-id="547da-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="547da-139">-파티션 버전</span><span class="sxs-lookup"><span data-stu-id="547da-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="547da-140">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="547da-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="547da-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547da-141">-ResourceGroupName</span></span>
<span data-ttu-id="547da-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-142">Name of resource group.</span></span>

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

### <span data-ttu-id="547da-143">-처리량</span><span class="sxs-lookup"><span data-stu-id="547da-143">-Throughput</span></span>
<span data-ttu-id="547da-144">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="547da-145">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-145">Default value is 400.</span></span>

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

### <span data-ttu-id="547da-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="547da-146">-TtlInSeconds</span></span>
<span data-ttu-id="547da-147">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="547da-148">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="547da-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="547da-149">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="547da-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="547da-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="547da-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="547da-151">UniqueKeyPolicy. CosmosDB. PSSqlUniqueKeyPolicy의 형식 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="547da-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="547da-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="547da-152">-WhatIf</span></span>
<span data-ttu-id="547da-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="547da-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="547da-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="547da-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="547da-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547da-155">CommonParameters</span></span>
<span data-ttu-id="547da-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="547da-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547da-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="547da-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547da-158">입력</span><span class="sxs-lookup"><span data-stu-id="547da-158">INPUTS</span></span>

### <span data-ttu-id="547da-159">않아야</span><span class="sxs-lookup"><span data-stu-id="547da-159">None</span></span>

## <span data-ttu-id="547da-160">출력</span><span class="sxs-lookup"><span data-stu-id="547da-160">OUTPUTS</span></span>

### <span data-ttu-id="547da-161">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="547da-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="547da-162">상속자</span><span class="sxs-lookup"><span data-stu-id="547da-162">NOTES</span></span>

## <span data-ttu-id="547da-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="547da-163">RELATED LINKS</span></span>
