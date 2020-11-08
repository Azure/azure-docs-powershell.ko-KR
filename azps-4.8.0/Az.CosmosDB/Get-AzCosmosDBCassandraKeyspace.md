---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212399"
---
# <span data-ttu-id="7f3b1-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="7f3b1-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="7f3b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3b1-103">CosmosDB Cassandra Keyspace를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="7f3b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f3b1-104">SYNTAX</span></span>

### <span data-ttu-id="7f3b1-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f3b1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f3b1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f3b1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7f3b1-107">DESCRIPTION</span></span>
<span data-ttu-id="7f3b1-108">**AzCosmosDBCassandraKeyspace** cmdlet은 새를 만들거나 기존 CosmosDB Cassandra Keyspace를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="7f3b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7f3b1-109">EXAMPLES</span></span>

### <span data-ttu-id="7f3b1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f3b1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="7f3b1-111">Get-AzCosmosDBCassandraKeyspace 기존 CassandraKeyspace의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="7f3b1-112">리소스를 확장 하 여 _etag, _ts _rid 속성을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="7f3b1-113">변수</span><span class="sxs-lookup"><span data-stu-id="7f3b1-113">PARAMETERS</span></span>

### <span data-ttu-id="7f3b1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f3b1-114">-AccountName</span></span>
<span data-ttu-id="7f3b1-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7f3b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3b1-116">-DefaultProfile</span></span>
<span data-ttu-id="7f3b1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3b1-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7f3b1-118">-Name</span></span>
<span data-ttu-id="7f3b1-119">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7f3b1-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7f3b1-120">-ParentObject</span></span>
<span data-ttu-id="7f3b1-121">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="7f3b1-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7f3b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f3b1-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-123">Name of resource group.</span></span>

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

### <span data-ttu-id="7f3b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3b1-124">CommonParameters</span></span>
<span data-ttu-id="7f3b1-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3b1-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3b1-127">입력</span><span class="sxs-lookup"><span data-stu-id="7f3b1-127">INPUTS</span></span>

### <span data-ttu-id="7f3b1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7f3b1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7f3b1-129">출력</span><span class="sxs-lookup"><span data-stu-id="7f3b1-129">OUTPUTS</span></span>

### <span data-ttu-id="7f3b1-130">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="7f3b1-131">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="7f3b1-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7f3b1-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7f3b1-132">NOTES</span></span>

## <span data-ttu-id="7f3b1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f3b1-133">RELATED LINKS</span></span>
