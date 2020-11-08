---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: d1b0dcee6c4337a572f98a51cb03c3fcdcd6c84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044440"
---
# <span data-ttu-id="a6bba-101">Set-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="a6bba-101">Set-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="a6bba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6bba-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bba-103">CosmosDB Cassandra Keyspace를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-103">Sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a6bba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6bba-104">SYNTAX</span></span>

### <span data-ttu-id="a6bba-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a6bba-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6bba-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6bba-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6bba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a6bba-107">DESCRIPTION</span></span>
<span data-ttu-id="a6bba-108">**Set-AzCosmosDBCassandraKeyspace** Cmdlet은 CosmosDB Cassandra Keyspace를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-108">The **Set-AzCosmosDBCassandraKeyspace** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a6bba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a6bba-109">EXAMPLES</span></span>

### <span data-ttu-id="a6bba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6bba-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraKeyspace -ResourceGroupName {rgName} -AccountName {accountName} -Name {keyspaceName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

<span data-ttu-id="a6bba-111">Resource 개체에는 _rid, _ts _etag 속성 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-111">Resource object contains the values of the _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="a6bba-112">변수</span><span class="sxs-lookup"><span data-stu-id="a6bba-112">PARAMETERS</span></span>

### <span data-ttu-id="a6bba-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6bba-113">-AccountName</span></span>
<span data-ttu-id="a6bba-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a6bba-115">-확인</span><span class="sxs-lookup"><span data-stu-id="a6bba-115">-Confirm</span></span>
<span data-ttu-id="a6bba-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bba-117">-DefaultProfile</span></span>
<span data-ttu-id="a6bba-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6bba-119">-InputObject</span></span>
<span data-ttu-id="a6bba-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="a6bba-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6bba-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a6bba-121">-Name</span></span>
<span data-ttu-id="a6bba-122">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="a6bba-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a6bba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bba-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6bba-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-124">Name of resource group.</span></span>

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

### <span data-ttu-id="a6bba-125">-처리량</span><span class="sxs-lookup"><span data-stu-id="a6bba-125">-Throughput</span></span>
<span data-ttu-id="a6bba-126">Cassandra Keyspace (a r/s)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="a6bba-127">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-127">Default value is 400.</span></span>

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

### <span data-ttu-id="a6bba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bba-128">-WhatIf</span></span>
<span data-ttu-id="a6bba-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bba-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bba-131">CommonParameters</span></span>
<span data-ttu-id="a6bba-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6bba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bba-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6bba-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bba-134">입력</span><span class="sxs-lookup"><span data-stu-id="a6bba-134">INPUTS</span></span>

### <span data-ttu-id="a6bba-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a6bba-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a6bba-136">출력</span><span class="sxs-lookup"><span data-stu-id="a6bba-136">OUTPUTS</span></span>

### <span data-ttu-id="a6bba-137">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="a6bba-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="a6bba-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a6bba-138">NOTES</span></span>

## <span data-ttu-id="a6bba-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6bba-139">RELATED LINKS</span></span>
