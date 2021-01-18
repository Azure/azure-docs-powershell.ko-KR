---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495816"
---
# <span data-ttu-id="b917e-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="b917e-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="b917e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b917e-102">SYNOPSIS</span></span>
<span data-ttu-id="b917e-103">이 기능을 사용하여 자동 조정된 데이터로 자동 조정된 데이터를 수동으로 마이그레이션하거나 그 반대로 마이그레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="b917e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b917e-104">SYNTAX</span></span>

### <span data-ttu-id="b917e-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b917e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b917e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b917e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b917e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b917e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b917e-108">설명</span><span class="sxs-lookup"><span data-stu-id="b917e-108">DESCRIPTION</span></span>
<span data-ttu-id="b917e-109">ThroughpyteType paramter는 마이그레이션하려는 데이터 양을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="b917e-110">예제</span><span class="sxs-lookup"><span data-stu-id="b917e-110">EXAMPLES</span></span>

### <span data-ttu-id="b917e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b917e-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="b917e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b917e-112">PARAMETERS</span></span>

### <span data-ttu-id="b917e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b917e-113">-AccountName</span></span>
<span data-ttu-id="b917e-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b917e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b917e-115">-Confirm</span></span>
<span data-ttu-id="b917e-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b917e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b917e-117">-DefaultProfile</span></span>
<span data-ttu-id="b917e-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b917e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b917e-119">-InputObject</span></span>
<span data-ttu-id="b917e-120">Cassandra Table 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b917e-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="b917e-121">-KeyspaceName</span></span>
<span data-ttu-id="b917e-122">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b917e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b917e-123">-Name</span></span>
<span data-ttu-id="b917e-124">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="b917e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b917e-125">-ParentObject</span></span>
<span data-ttu-id="b917e-126">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="b917e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b917e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b917e-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b917e-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="b917e-129">-ThroughputType</span></span>
<span data-ttu-id="b917e-130">마이그레이션할 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="b917e-131">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="b917e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b917e-132">-WhatIf</span></span>
<span data-ttu-id="b917e-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b917e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b917e-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b917e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b917e-135">CommonParameters</span></span>
<span data-ttu-id="b917e-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b917e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b917e-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b917e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b917e-138">입력</span><span class="sxs-lookup"><span data-stu-id="b917e-138">INPUTS</span></span>

### <span data-ttu-id="b917e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="b917e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="b917e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b917e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="b917e-141">출력</span><span class="sxs-lookup"><span data-stu-id="b917e-141">OUTPUTS</span></span>

### <span data-ttu-id="b917e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b917e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b917e-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b917e-143">NOTES</span></span>

## <span data-ttu-id="b917e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b917e-144">RELATED LINKS</span></span>
