---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337934"
---
# <span data-ttu-id="31e9c-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="31e9c-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="31e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="31e9c-103">CosmosDB Cassandra 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="31e9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="31e9c-104">SYNTAX</span></span>

### <span data-ttu-id="31e9c-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="31e9c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e9c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31e9c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e9c-107">설명</span><span class="sxs-lookup"><span data-stu-id="31e9c-107">DESCRIPTION</span></span>
<span data-ttu-id="31e9c-108">**Get-AzCosmosDBCassandraTable** cmdlet은 새 CosmosDB Cassandra Keyspace를 새로 생성하거나 기존 CosmosDB Cassandra Keyspace를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="31e9c-109">예제</span><span class="sxs-lookup"><span data-stu-id="31e9c-109">EXAMPLES</span></span>

### <span data-ttu-id="31e9c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="31e9c-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="31e9c-111">{{ Get-AzCosmosDBCassandraTable CassandraKeyspace의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="31e9c-112">Resource를 확장하여 DefaultTtl, Schema, _etag, _ts, _rid properties.}를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="31e9c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31e9c-113">PARAMETERS</span></span>

### <span data-ttu-id="31e9c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31e9c-114">-AccountName</span></span>
<span data-ttu-id="31e9c-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="31e9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e9c-116">-DefaultProfile</span></span>
<span data-ttu-id="31e9c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e9c-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="31e9c-118">-KeyspaceName</span></span>
<span data-ttu-id="31e9c-119">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="31e9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="31e9c-120">-Name</span></span>
<span data-ttu-id="31e9c-121">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="31e9c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="31e9c-122">-ParentObject</span></span>
<span data-ttu-id="31e9c-123">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="31e9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="31e9c-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="31e9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e9c-126">CommonParameters</span></span>
<span data-ttu-id="31e9c-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31e9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e9c-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31e9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e9c-129">입력</span><span class="sxs-lookup"><span data-stu-id="31e9c-129">INPUTS</span></span>

### <span data-ttu-id="31e9c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="31e9c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="31e9c-131">출력</span><span class="sxs-lookup"><span data-stu-id="31e9c-131">OUTPUTS</span></span>

### <span data-ttu-id="31e9c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="31e9c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="31e9c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="31e9c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="31e9c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31e9c-134">NOTES</span></span>

## <span data-ttu-id="31e9c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31e9c-135">RELATED LINKS</span></span>
