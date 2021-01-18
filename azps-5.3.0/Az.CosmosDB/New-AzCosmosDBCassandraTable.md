---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495801"
---
# <span data-ttu-id="ffdd9-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="ffdd9-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="ffdd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdd9-103">새 CosmosDB Cassandra 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="ffdd9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ffdd9-104">SYNTAX</span></span>

### <span data-ttu-id="ffdd9-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ffdd9-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffdd9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffdd9-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffdd9-107">설명</span><span class="sxs-lookup"><span data-stu-id="ffdd9-107">DESCRIPTION</span></span>
<span data-ttu-id="ffdd9-108">새 CosmosDB Cassandra 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="ffdd9-109">예제</span><span class="sxs-lookup"><span data-stu-id="ffdd9-109">EXAMPLES</span></span>

### <span data-ttu-id="ffdd9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffdd9-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="ffdd9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffdd9-111">PARAMETERS</span></span>

### <span data-ttu-id="ffdd9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ffdd9-112">-AccountName</span></span>
<span data-ttu-id="ffdd9-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ffdd9-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="ffdd9-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="ffdd9-115">분석 저장소 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="ffdd9-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ffdd9-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ffdd9-117">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ffdd9-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffdd9-118">-Confirm</span></span>
<span data-ttu-id="ffdd9-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffdd9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdd9-120">-DefaultProfile</span></span>
<span data-ttu-id="ffdd9-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffdd9-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="ffdd9-122">-KeyspaceName</span></span>
<span data-ttu-id="ffdd9-123">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="ffdd9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ffdd9-124">-Name</span></span>
<span data-ttu-id="ffdd9-125">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="ffdd9-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ffdd9-126">-ParentObject</span></span>
<span data-ttu-id="ffdd9-127">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-127">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffdd9-128">-ResourceGroupName</span></span>
<span data-ttu-id="ffdd9-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-129">Name of resource group.</span></span>

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

### <span data-ttu-id="ffdd9-130">-Schema</span><span class="sxs-lookup"><span data-stu-id="ffdd9-130">-Schema</span></span>
<span data-ttu-id="ffdd9-131">PSCassandraSchema 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="ffdd9-132">이 New-AzCosmosDBCassandraSchema 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-133">-Throughput</span><span class="sxs-lookup"><span data-stu-id="ffdd9-133">-Throughput</span></span>
<span data-ttu-id="ffdd9-134">Cassandra Keyspace(RU/s)의 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="ffdd9-135">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-135">Default value is 400.</span></span>

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

### <span data-ttu-id="ffdd9-136">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="ffdd9-136">-TtlInSeconds</span></span>
<span data-ttu-id="ffdd9-137">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="ffdd9-138">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="ffdd9-139">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="ffdd9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffdd9-140">-WhatIf</span></span>
<span data-ttu-id="ffdd9-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ffdd9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffdd9-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffdd9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdd9-143">CommonParameters</span></span>
<span data-ttu-id="ffdd9-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdd9-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdd9-146">입력</span><span class="sxs-lookup"><span data-stu-id="ffdd9-146">INPUTS</span></span>

### <span data-ttu-id="ffdd9-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="ffdd9-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="ffdd9-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ffdd9-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="ffdd9-149">출력</span><span class="sxs-lookup"><span data-stu-id="ffdd9-149">OUTPUTS</span></span>

### <span data-ttu-id="ffdd9-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="ffdd9-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="ffdd9-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="ffdd9-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="ffdd9-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ffdd9-152">NOTES</span></span>

## <span data-ttu-id="ffdd9-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffdd9-153">RELATED LINKS</span></span>
