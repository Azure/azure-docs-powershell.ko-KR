---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044423"
---
# <span data-ttu-id="9104c-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="9104c-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="9104c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9104c-102">SYNOPSIS</span></span>
<span data-ttu-id="9104c-103">CosmosDB Cassandra 테이블의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="9104c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9104c-104">SYNTAX</span></span>

### <span data-ttu-id="9104c-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9104c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9104c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9104c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9104c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9104c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9104c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9104c-108">EXAMPLES</span></span>

### <span data-ttu-id="9104c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="9104c-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="9104c-110">변수</span><span class="sxs-lookup"><span data-stu-id="9104c-110">PARAMETERS</span></span>

### <span data-ttu-id="9104c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9104c-111">-AccountName</span></span>
<span data-ttu-id="9104c-112">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9104c-113">-확인</span><span class="sxs-lookup"><span data-stu-id="9104c-113">-Confirm</span></span>
<span data-ttu-id="9104c-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9104c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9104c-115">-DefaultProfile</span></span>
<span data-ttu-id="9104c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9104c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9104c-117">-InputObject</span></span>
<span data-ttu-id="9104c-118">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-118">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9104c-119">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="9104c-119">-KeyspaceName</span></span>
<span data-ttu-id="9104c-120">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="9104c-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9104c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9104c-121">-Name</span></span>
<span data-ttu-id="9104c-122">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="9104c-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9104c-123">-ParentObject</span></span>
<span data-ttu-id="9104c-124">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9104c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9104c-125">-ResourceGroupName</span></span>
<span data-ttu-id="9104c-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9104c-127">-처리량</span><span class="sxs-lookup"><span data-stu-id="9104c-127">-Throughput</span></span>
<span data-ttu-id="9104c-128">Cassandra Keyspace (a r/s)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9104c-129">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9104c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9104c-130">-WhatIf</span></span>
<span data-ttu-id="9104c-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9104c-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9104c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9104c-133">CommonParameters</span></span>
<span data-ttu-id="9104c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9104c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9104c-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9104c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9104c-136">입력</span><span class="sxs-lookup"><span data-stu-id="9104c-136">INPUTS</span></span>

### <span data-ttu-id="9104c-137">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9104c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9104c-138">출력</span><span class="sxs-lookup"><span data-stu-id="9104c-138">OUTPUTS</span></span>

### <span data-ttu-id="9104c-139">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9104c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9104c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9104c-140">NOTES</span></span>

## <span data-ttu-id="9104c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9104c-141">RELATED LINKS</span></span>
