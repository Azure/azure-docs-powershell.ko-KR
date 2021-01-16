---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344642"
---
# <span data-ttu-id="0ad6c-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="0ad6c-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="0ad6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad6c-103">CosmosDB Cassandra 테이블의 진행 값도 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0ad6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ad6c-104">SYNTAX</span></span>

### <span data-ttu-id="0ad6c-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ad6c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad6c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ad6c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad6c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ad6c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad6c-108">설명</span><span class="sxs-lookup"><span data-stu-id="0ad6c-108">DESCRIPTION</span></span>
<span data-ttu-id="0ad6c-109">CosmosDB Cassandra 테이블의 진행 값도 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="0ad6c-110">예제</span><span class="sxs-lookup"><span data-stu-id="0ad6c-110">EXAMPLES</span></span>

### <span data-ttu-id="0ad6c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ad6c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="0ad6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ad6c-112">PARAMETERS</span></span>

### <span data-ttu-id="0ad6c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0ad6c-113">-AccountName</span></span>
<span data-ttu-id="0ad6c-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0ad6c-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0ad6c-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0ad6c-116">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0ad6c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ad6c-117">-Confirm</span></span>
<span data-ttu-id="0ad6c-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad6c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad6c-119">-DefaultProfile</span></span>
<span data-ttu-id="0ad6c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad6c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad6c-121">-InputObject</span></span>
<span data-ttu-id="0ad6c-122">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="0ad6c-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="0ad6c-123">-KeyspaceName</span></span>
<span data-ttu-id="0ad6c-124">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0ad6c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0ad6c-125">-Name</span></span>
<span data-ttu-id="0ad6c-126">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="0ad6c-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0ad6c-127">-ParentObject</span></span>
<span data-ttu-id="0ad6c-128">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="0ad6c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad6c-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ad6c-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="0ad6c-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="0ad6c-131">-Throughput</span></span>
<span data-ttu-id="0ad6c-132">Cassandra Keyspace(RU/s)의 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="0ad6c-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-133">Default value is 400.</span></span>

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

### <span data-ttu-id="0ad6c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad6c-134">-WhatIf</span></span>
<span data-ttu-id="0ad6c-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0ad6c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ad6c-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad6c-137">CommonParameters</span></span>
<span data-ttu-id="0ad6c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad6c-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ad6c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad6c-140">입력</span><span class="sxs-lookup"><span data-stu-id="0ad6c-140">INPUTS</span></span>

### <span data-ttu-id="0ad6c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0ad6c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="0ad6c-142">출력</span><span class="sxs-lookup"><span data-stu-id="0ad6c-142">OUTPUTS</span></span>

### <span data-ttu-id="0ad6c-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0ad6c-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0ad6c-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ad6c-144">NOTES</span></span>

## <span data-ttu-id="0ad6c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ad6c-145">RELATED LINKS</span></span>
