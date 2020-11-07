---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877873"
---
# <span data-ttu-id="6ddfc-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="6ddfc-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="6ddfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ddfc-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddfc-103">CosmosDB Cassandra Keyspace를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6ddfc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ddfc-104">SYNTAX</span></span>

### <span data-ttu-id="6ddfc-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ddfc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddfc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ddfc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ddfc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6ddfc-107">DESCRIPTION</span></span>
<span data-ttu-id="6ddfc-108">**AzCosmosDBCassandraKeyspace** cmdlet은 새를 만들거나 기존 CosmosDB Cassandra Keyspace를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="6ddfc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6ddfc-109">EXAMPLES</span></span>

### <span data-ttu-id="6ddfc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ddfc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="6ddfc-111">Get-AzCosmosDBCassandraKeyspace 기존 CassandraKeyspace의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="6ddfc-112">리소스를 확장 하 여 _etag, _ts _rid 속성을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="6ddfc-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ddfc-113">PARAMETERS</span></span>

### <span data-ttu-id="6ddfc-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ddfc-114">-AccountName</span></span>
<span data-ttu-id="6ddfc-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6ddfc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddfc-116">-DefaultProfile</span></span>
<span data-ttu-id="6ddfc-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ddfc-118">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="6ddfc-118">-Detailed</span></span>
<span data-ttu-id="6ddfc-119">그런 다음 cmdlet은 해당 처리 값이 포함 된 Keyspace를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="6ddfc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ddfc-120">-InputObject</span></span>
<span data-ttu-id="6ddfc-121">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="6ddfc-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6ddfc-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6ddfc-122">-Name</span></span>
<span data-ttu-id="6ddfc-123">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6ddfc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ddfc-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ddfc-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-125">Name of resource group.</span></span>

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

### <span data-ttu-id="6ddfc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddfc-126">CommonParameters</span></span>
<span data-ttu-id="6ddfc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddfc-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddfc-129">입력</span><span class="sxs-lookup"><span data-stu-id="6ddfc-129">INPUTS</span></span>

### <span data-ttu-id="6ddfc-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6ddfc-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6ddfc-131">출력</span><span class="sxs-lookup"><span data-stu-id="6ddfc-131">OUTPUTS</span></span>

### <span data-ttu-id="6ddfc-132">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="6ddfc-133">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6ddfc-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6ddfc-134">상속자</span><span class="sxs-lookup"><span data-stu-id="6ddfc-134">NOTES</span></span>

## <span data-ttu-id="6ddfc-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ddfc-135">RELATED LINKS</span></span>
