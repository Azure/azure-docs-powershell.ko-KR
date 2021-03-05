---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: fb387adafa1a1a71d9a42b09b8c7255955eccd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978747"
---
# <span data-ttu-id="9805a-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="9805a-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="9805a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9805a-102">SYNOPSIS</span></span>
<span data-ttu-id="9805a-103">CosmosDB Cassandra 키스페이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9805a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9805a-104">SYNTAX</span></span>

### <span data-ttu-id="9805a-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9805a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9805a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9805a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9805a-107">설명</span><span class="sxs-lookup"><span data-stu-id="9805a-107">DESCRIPTION</span></span>
<span data-ttu-id="9805a-108">**Get-AzCosmosDBCassandraKeyspace** cmdlet은 기존 CosmosDB Cassandra 키스페이스를 새로 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9805a-109">예제</span><span class="sxs-lookup"><span data-stu-id="9805a-109">EXAMPLES</span></span>

### <span data-ttu-id="9805a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9805a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="9805a-111">Get-AzCosmosDBCassandraKeyspace CassandraKeyspace의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="9805a-112">리소스를 확장하여 _etag, _ts _rid 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="9805a-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9805a-113">PARAMETERS</span></span>

### <span data-ttu-id="9805a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9805a-114">-AccountName</span></span>
<span data-ttu-id="9805a-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9805a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9805a-116">-DefaultProfile</span></span>
<span data-ttu-id="9805a-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9805a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9805a-118">-Name</span></span>
<span data-ttu-id="9805a-119">Cassandra 키스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9805a-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9805a-120">-ParentObject</span></span>
<span data-ttu-id="9805a-121">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="9805a-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9805a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9805a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9805a-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-123">Name of resource group.</span></span>

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

### <span data-ttu-id="9805a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9805a-124">CommonParameters</span></span>
<span data-ttu-id="9805a-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9805a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9805a-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9805a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9805a-127">입력</span><span class="sxs-lookup"><span data-stu-id="9805a-127">INPUTS</span></span>

### <span data-ttu-id="9805a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9805a-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9805a-129">출력</span><span class="sxs-lookup"><span data-stu-id="9805a-129">OUTPUTS</span></span>

### <span data-ttu-id="9805a-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9805a-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="9805a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9805a-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9805a-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9805a-132">NOTES</span></span>

## <span data-ttu-id="9805a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9805a-133">RELATED LINKS</span></span>
