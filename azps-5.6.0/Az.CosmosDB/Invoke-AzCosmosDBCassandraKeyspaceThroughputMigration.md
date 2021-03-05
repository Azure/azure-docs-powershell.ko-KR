---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: d14df15f40eedab68af3d0cd6bfa0672b6283652
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977467"
---
# <span data-ttu-id="26339-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="26339-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="26339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26339-102">SYNOPSIS</span></span>
<span data-ttu-id="26339-103">이 방법을 사용하여 자동 조정된 작업량은 수동 작업량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="26339-104">구문</span><span class="sxs-lookup"><span data-stu-id="26339-104">SYNTAX</span></span>

### <span data-ttu-id="26339-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="26339-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26339-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26339-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26339-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26339-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26339-108">설명</span><span class="sxs-lookup"><span data-stu-id="26339-108">DESCRIPTION</span></span>
<span data-ttu-id="26339-109">ThroughpyteType paramter는 마이그레이션할 수 있는 이루어 를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="26339-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="26339-110">예제</span><span class="sxs-lookup"><span data-stu-id="26339-110">EXAMPLES</span></span>

### <span data-ttu-id="26339-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="26339-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="26339-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26339-112">PARAMETERS</span></span>

### <span data-ttu-id="26339-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26339-113">-AccountName</span></span>
<span data-ttu-id="26339-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26339-115">-확인</span><span class="sxs-lookup"><span data-stu-id="26339-115">-Confirm</span></span>
<span data-ttu-id="26339-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26339-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26339-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26339-117">-DefaultProfile</span></span>
<span data-ttu-id="26339-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26339-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26339-119">-InputObject</span></span>
<span data-ttu-id="26339-120">Cassandra 키스페이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26339-121">-Name</span><span class="sxs-lookup"><span data-stu-id="26339-121">-Name</span></span>
<span data-ttu-id="26339-122">Cassandra 키스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="26339-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="26339-123">-ParentObject</span></span>
<span data-ttu-id="26339-124">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="26339-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26339-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26339-125">-ResourceGroupName</span></span>
<span data-ttu-id="26339-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-126">Name of resource group.</span></span>

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

### <span data-ttu-id="26339-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="26339-127">-ThroughputType</span></span>
<span data-ttu-id="26339-128">마이그레이션할 수 있는 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="26339-129">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="26339-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="26339-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26339-130">-WhatIf</span></span>
<span data-ttu-id="26339-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="26339-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26339-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26339-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26339-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26339-133">CommonParameters</span></span>
<span data-ttu-id="26339-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26339-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26339-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26339-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26339-136">입력</span><span class="sxs-lookup"><span data-stu-id="26339-136">INPUTS</span></span>

### <span data-ttu-id="26339-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="26339-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="26339-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="26339-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="26339-139">출력</span><span class="sxs-lookup"><span data-stu-id="26339-139">OUTPUTS</span></span>

### <span data-ttu-id="26339-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="26339-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="26339-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26339-141">NOTES</span></span>

## <span data-ttu-id="26339-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26339-142">RELATED LINKS</span></span>
