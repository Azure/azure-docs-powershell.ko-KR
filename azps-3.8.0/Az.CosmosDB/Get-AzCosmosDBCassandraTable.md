---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044127"
---
# <span data-ttu-id="316d7-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="316d7-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="316d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="316d7-102">SYNOPSIS</span></span>
<span data-ttu-id="316d7-103">CosmosDB Cassandra 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="316d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="316d7-104">SYNTAX</span></span>

### <span data-ttu-id="316d7-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="316d7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="316d7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="316d7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316d7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="316d7-107">DESCRIPTION</span></span>
<span data-ttu-id="316d7-108">**AzCosmosDBCassandraTable** cmdlet은 새를 만들거나 기존 CosmosDB Cassandra Keyspace를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="316d7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="316d7-109">EXAMPLES</span></span>

### <span data-ttu-id="316d7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="316d7-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="316d7-111">{{Get-AzCosmosDBCassandraTable는 기존 CassandraKeyspace의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="316d7-112">리소스를 확장 하 여 DefaultTtl, Schema, _etag, _ts _rid 속성을 가져올 수 있습니다.}}</span><span class="sxs-lookup"><span data-stu-id="316d7-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="316d7-113">변수</span><span class="sxs-lookup"><span data-stu-id="316d7-113">PARAMETERS</span></span>

### <span data-ttu-id="316d7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="316d7-114">-AccountName</span></span>
<span data-ttu-id="316d7-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="316d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316d7-116">-DefaultProfile</span></span>
<span data-ttu-id="316d7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316d7-118">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="316d7-118">-Detailed</span></span>
<span data-ttu-id="316d7-119">그런 다음 cmdlet은 해당 처리 값이 지정 된 Cassandra 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316d7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="316d7-120">-InputObject</span></span>
<span data-ttu-id="316d7-121">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-121">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="316d7-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="316d7-122">-KeyspaceName</span></span>
<span data-ttu-id="316d7-123">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="316d7-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="316d7-124">-이름</span><span class="sxs-lookup"><span data-stu-id="316d7-124">-Name</span></span>
<span data-ttu-id="316d7-125">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="316d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="316d7-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-127">Name of resource group.</span></span>

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

### <span data-ttu-id="316d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316d7-128">CommonParameters</span></span>
<span data-ttu-id="316d7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="316d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316d7-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="316d7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316d7-131">입력</span><span class="sxs-lookup"><span data-stu-id="316d7-131">INPUTS</span></span>

### <span data-ttu-id="316d7-132">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="316d7-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="316d7-133">출력</span><span class="sxs-lookup"><span data-stu-id="316d7-133">OUTPUTS</span></span>

### <span data-ttu-id="316d7-134">CosmosDB. PSCassandraTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="316d7-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="316d7-135">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="316d7-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="316d7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="316d7-136">NOTES</span></span>

## <span data-ttu-id="316d7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="316d7-137">RELATED LINKS</span></span>
