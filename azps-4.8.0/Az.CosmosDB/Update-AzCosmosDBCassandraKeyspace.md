---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212372"
---
# <span data-ttu-id="7f179-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="7f179-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="7f179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f179-102">SYNOPSIS</span></span>
<span data-ttu-id="7f179-103">CosmosDB Cassandra Keyspace를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="7f179-104">기존 Keyspace를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="7f179-105">구문과</span><span class="sxs-lookup"><span data-stu-id="7f179-105">SYNTAX</span></span>

### <span data-ttu-id="7f179-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f179-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f179-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f179-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f179-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f179-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f179-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7f179-109">DESCRIPTION</span></span>
<span data-ttu-id="7f179-110">CosmosDB Cassandra Keyspace를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="7f179-111">기존 Keyspace를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="7f179-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7f179-112">EXAMPLES</span></span>

### <span data-ttu-id="7f179-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f179-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="7f179-114">변수</span><span class="sxs-lookup"><span data-stu-id="7f179-114">PARAMETERS</span></span>

### <span data-ttu-id="7f179-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f179-115">-AccountName</span></span>
<span data-ttu-id="7f179-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7f179-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7f179-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7f179-118">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7f179-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7f179-119">-Confirm</span></span>
<span data-ttu-id="7f179-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f179-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f179-121">-DefaultProfile</span></span>
<span data-ttu-id="7f179-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f179-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f179-123">-InputObject</span></span>
<span data-ttu-id="7f179-124">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="7f179-125">-이름</span><span class="sxs-lookup"><span data-stu-id="7f179-125">-Name</span></span>
<span data-ttu-id="7f179-126">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="7f179-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7f179-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7f179-127">-ParentObject</span></span>
<span data-ttu-id="7f179-128">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="7f179-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7f179-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f179-129">-ResourceGroupName</span></span>
<span data-ttu-id="7f179-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7f179-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="7f179-131">-Throughput</span></span>
<span data-ttu-id="7f179-132">Cassandra Keyspace (a r/s)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="7f179-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-133">Default value is 400.</span></span>

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

### <span data-ttu-id="7f179-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f179-134">-WhatIf</span></span>
<span data-ttu-id="7f179-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f179-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f179-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f179-137">CommonParameters</span></span>
<span data-ttu-id="7f179-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f179-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f179-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f179-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f179-140">입력</span><span class="sxs-lookup"><span data-stu-id="7f179-140">INPUTS</span></span>

### <span data-ttu-id="7f179-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7f179-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="7f179-142">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="7f179-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="7f179-143">출력</span><span class="sxs-lookup"><span data-stu-id="7f179-143">OUTPUTS</span></span>

### <span data-ttu-id="7f179-144">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="7f179-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="7f179-145">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="7f179-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7f179-146">상속자</span><span class="sxs-lookup"><span data-stu-id="7f179-146">NOTES</span></span>

## <span data-ttu-id="7f179-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f179-147">RELATED LINKS</span></span>
