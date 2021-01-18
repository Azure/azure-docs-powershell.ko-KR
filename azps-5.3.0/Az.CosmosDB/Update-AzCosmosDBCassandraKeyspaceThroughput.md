---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493657"
---
# <span data-ttu-id="dc844-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="dc844-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="dc844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc844-102">SYNOPSIS</span></span>
<span data-ttu-id="dc844-103">CosmosDB Cassandra Keyspace의 사용료 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="dc844-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc844-104">SYNTAX</span></span>

### <span data-ttu-id="dc844-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc844-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc844-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc844-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc844-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc844-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc844-108">설명</span><span class="sxs-lookup"><span data-stu-id="dc844-108">DESCRIPTION</span></span>
<span data-ttu-id="dc844-109">CosmosDB Cassandra Keyspace의 사용료 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="dc844-110">예제</span><span class="sxs-lookup"><span data-stu-id="dc844-110">EXAMPLES</span></span>

### <span data-ttu-id="dc844-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc844-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="dc844-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc844-112">PARAMETERS</span></span>

### <span data-ttu-id="dc844-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc844-113">-AccountName</span></span>
<span data-ttu-id="dc844-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc844-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="dc844-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="dc844-116">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="dc844-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc844-117">-Confirm</span></span>
<span data-ttu-id="dc844-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc844-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc844-119">-DefaultProfile</span></span>
<span data-ttu-id="dc844-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc844-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc844-121">-InputObject</span></span>
<span data-ttu-id="dc844-122">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="dc844-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dc844-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dc844-123">-Name</span></span>
<span data-ttu-id="dc844-124">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="dc844-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc844-125">-ParentObject</span></span>
<span data-ttu-id="dc844-126">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="dc844-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="dc844-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc844-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc844-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-128">Name of resource group.</span></span>

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

### <span data-ttu-id="dc844-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="dc844-129">-Throughput</span></span>
<span data-ttu-id="dc844-130">Cassandra Keyspace(RU/s)의 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="dc844-131">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-131">Default value is 400.</span></span>

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

### <span data-ttu-id="dc844-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc844-132">-WhatIf</span></span>
<span data-ttu-id="dc844-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc844-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc844-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc844-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc844-135">CommonParameters</span></span>
<span data-ttu-id="dc844-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc844-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc844-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc844-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc844-138">입력</span><span class="sxs-lookup"><span data-stu-id="dc844-138">INPUTS</span></span>

### <span data-ttu-id="dc844-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="dc844-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="dc844-140">출력</span><span class="sxs-lookup"><span data-stu-id="dc844-140">OUTPUTS</span></span>

### <span data-ttu-id="dc844-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dc844-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dc844-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc844-142">NOTES</span></span>

## <span data-ttu-id="dc844-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc844-143">RELATED LINKS</span></span>
