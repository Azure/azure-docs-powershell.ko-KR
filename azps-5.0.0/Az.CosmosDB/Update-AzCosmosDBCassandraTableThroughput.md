---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306830"
---
# <span data-ttu-id="85936-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="85936-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="85936-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85936-102">SYNOPSIS</span></span>
<span data-ttu-id="85936-103">CosmosDB Cassandra 테이블의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="85936-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="85936-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85936-104">SYNTAX</span></span>

### <span data-ttu-id="85936-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="85936-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85936-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85936-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85936-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85936-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85936-108">설명은</span><span class="sxs-lookup"><span data-stu-id="85936-108">DESCRIPTION</span></span>
<span data-ttu-id="85936-109">CosmosDB Cassandra 테이블의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="85936-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="85936-110">예제의</span><span class="sxs-lookup"><span data-stu-id="85936-110">EXAMPLES</span></span>

### <span data-ttu-id="85936-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="85936-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="85936-112">변수</span><span class="sxs-lookup"><span data-stu-id="85936-112">PARAMETERS</span></span>

### <span data-ttu-id="85936-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85936-113">-AccountName</span></span>
<span data-ttu-id="85936-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="85936-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="85936-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="85936-116">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="85936-117">-확인</span><span class="sxs-lookup"><span data-stu-id="85936-117">-Confirm</span></span>
<span data-ttu-id="85936-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85936-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85936-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85936-119">-DefaultProfile</span></span>
<span data-ttu-id="85936-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85936-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85936-121">-InputObject</span></span>
<span data-ttu-id="85936-122">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="85936-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="85936-123">-KeyspaceName</span></span>
<span data-ttu-id="85936-124">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="85936-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="85936-125">-이름</span><span class="sxs-lookup"><span data-stu-id="85936-125">-Name</span></span>
<span data-ttu-id="85936-126">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="85936-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="85936-127">-ParentObject</span></span>
<span data-ttu-id="85936-128">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="85936-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85936-129">-ResourceGroupName</span></span>
<span data-ttu-id="85936-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-130">Name of resource group.</span></span>

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

### <span data-ttu-id="85936-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="85936-131">-Throughput</span></span>
<span data-ttu-id="85936-132">Cassandra Keyspace (a r/s)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="85936-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="85936-133">Default value is 400.</span></span>

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

### <span data-ttu-id="85936-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85936-134">-WhatIf</span></span>
<span data-ttu-id="85936-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85936-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85936-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85936-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85936-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85936-137">CommonParameters</span></span>
<span data-ttu-id="85936-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85936-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85936-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85936-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85936-140">입력</span><span class="sxs-lookup"><span data-stu-id="85936-140">INPUTS</span></span>

### <span data-ttu-id="85936-141">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="85936-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="85936-142">출력</span><span class="sxs-lookup"><span data-stu-id="85936-142">OUTPUTS</span></span>

### <span data-ttu-id="85936-143">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="85936-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="85936-144">상속자</span><span class="sxs-lookup"><span data-stu-id="85936-144">NOTES</span></span>

## <span data-ttu-id="85936-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85936-145">RELATED LINKS</span></span>
