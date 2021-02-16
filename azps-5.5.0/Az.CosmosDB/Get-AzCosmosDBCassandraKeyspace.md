---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199068"
---
# <span data-ttu-id="d3a6b-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="d3a6b-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="d3a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a6b-103">CosmosDB Cassandra Keyspace를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d3a6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3a6b-104">SYNTAX</span></span>

### <span data-ttu-id="d3a6b-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3a6b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3a6b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a6b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a6b-107">설명</span><span class="sxs-lookup"><span data-stu-id="d3a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="d3a6b-108">**Get-AzCosmosDBCassandraKeyspace** cmdlet은 새 CosmosDB Cassandra Keyspace를 새로 생성하거나 기존 CosmosDB Cassandra Keyspace를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d3a6b-109">예제</span><span class="sxs-lookup"><span data-stu-id="d3a6b-109">EXAMPLES</span></span>

### <span data-ttu-id="d3a6b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3a6b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="d3a6b-111">Get-AzCosmosDBCassandraKeyspace CassandraKeyspace의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="d3a6b-112">리소스를 확장하여 리소스, _etag _ts _rid 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="d3a6b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a6b-113">PARAMETERS</span></span>

### <span data-ttu-id="d3a6b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3a6b-114">-AccountName</span></span>
<span data-ttu-id="d3a6b-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3a6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a6b-116">-DefaultProfile</span></span>
<span data-ttu-id="d3a6b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a6b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d3a6b-118">-Name</span></span>
<span data-ttu-id="d3a6b-119">Cassandra 키스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d3a6b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3a6b-120">-ParentObject</span></span>
<span data-ttu-id="d3a6b-121">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d3a6b-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d3a6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3a6b-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-123">Name of resource group.</span></span>

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

### <span data-ttu-id="d3a6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a6b-124">CommonParameters</span></span>
<span data-ttu-id="d3a6b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a6b-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3a6b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a6b-127">입력</span><span class="sxs-lookup"><span data-stu-id="d3a6b-127">INPUTS</span></span>

### <span data-ttu-id="d3a6b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d3a6b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d3a6b-129">출력</span><span class="sxs-lookup"><span data-stu-id="d3a6b-129">OUTPUTS</span></span>

### <span data-ttu-id="d3a6b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="d3a6b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="d3a6b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d3a6b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d3a6b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3a6b-132">NOTES</span></span>

## <span data-ttu-id="d3a6b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3a6b-133">RELATED LINKS</span></span>
