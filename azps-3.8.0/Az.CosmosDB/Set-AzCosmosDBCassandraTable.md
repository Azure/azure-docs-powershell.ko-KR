---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044439"
---
# <span data-ttu-id="cf24f-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="cf24f-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="cf24f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf24f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf24f-103">CosmosDB Cassandra 테이블을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="cf24f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf24f-104">SYNTAX</span></span>

### <span data-ttu-id="cf24f-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf24f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf24f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf24f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf24f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cf24f-107">DESCRIPTION</span></span>
<span data-ttu-id="cf24f-108">**Set-AzCosmosDBCassandraTable** Cmdlet은 CosmosDB Cassandra Keyspace를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="cf24f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cf24f-109">EXAMPLES</span></span>

### <span data-ttu-id="cf24f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf24f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="cf24f-111">Resource 개체에는 _rid, _ts, _etag, DefaultTtl, 스키마 속성 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="cf24f-112">변수</span><span class="sxs-lookup"><span data-stu-id="cf24f-112">PARAMETERS</span></span>

### <span data-ttu-id="cf24f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf24f-113">-AccountName</span></span>
<span data-ttu-id="cf24f-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cf24f-115">-확인</span><span class="sxs-lookup"><span data-stu-id="cf24f-115">-Confirm</span></span>
<span data-ttu-id="cf24f-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf24f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf24f-117">-DefaultProfile</span></span>
<span data-ttu-id="cf24f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf24f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf24f-119">-InputObject</span></span>
<span data-ttu-id="cf24f-120">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="cf24f-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="cf24f-121">-KeyspaceName</span></span>
<span data-ttu-id="cf24f-122">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="cf24f-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="cf24f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="cf24f-123">-Name</span></span>
<span data-ttu-id="cf24f-124">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="cf24f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf24f-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf24f-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-126">Name of resource group.</span></span>

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

### <span data-ttu-id="cf24f-127">-스키마</span><span class="sxs-lookup"><span data-stu-id="cf24f-127">-Schema</span></span>
<span data-ttu-id="cf24f-128">PSCassandraSchema 개체</span><span class="sxs-lookup"><span data-stu-id="cf24f-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="cf24f-129">이 개체를 만들려면 New-AzCosmosDBCassandraSchema를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="cf24f-130">-처리량</span><span class="sxs-lookup"><span data-stu-id="cf24f-130">-Throughput</span></span>
<span data-ttu-id="cf24f-131">Cassandra Keyspace (a r/s)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="cf24f-132">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-132">Default value is 400.</span></span>

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

### <span data-ttu-id="cf24f-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="cf24f-133">-TtlInSeconds</span></span>
<span data-ttu-id="cf24f-134">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="cf24f-135">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="cf24f-136">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="cf24f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf24f-137">-WhatIf</span></span>
<span data-ttu-id="cf24f-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf24f-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf24f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf24f-140">CommonParameters</span></span>
<span data-ttu-id="cf24f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf24f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf24f-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf24f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf24f-143">입력</span><span class="sxs-lookup"><span data-stu-id="cf24f-143">INPUTS</span></span>

### <span data-ttu-id="cf24f-144">CosmosDB. PSCassandraSchema/.</span><span class="sxs-lookup"><span data-stu-id="cf24f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="cf24f-145">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="cf24f-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="cf24f-146">출력</span><span class="sxs-lookup"><span data-stu-id="cf24f-146">OUTPUTS</span></span>

### <span data-ttu-id="cf24f-147">CosmosDB. PSCassandraTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="cf24f-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="cf24f-148">상속자</span><span class="sxs-lookup"><span data-stu-id="cf24f-148">NOTES</span></span>

## <span data-ttu-id="cf24f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf24f-149">RELATED LINKS</span></span>
