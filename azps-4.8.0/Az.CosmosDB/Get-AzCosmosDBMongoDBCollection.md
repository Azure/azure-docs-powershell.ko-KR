---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212567"
---
# <span data-ttu-id="778b6-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="778b6-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="778b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="778b6-102">SYNOPSIS</span></span>
<span data-ttu-id="778b6-103">CosmosDB MongoDB 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="778b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="778b6-104">SYNTAX</span></span>

### <span data-ttu-id="778b6-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="778b6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="778b6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="778b6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="778b6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="778b6-107">DESCRIPTION</span></span>
<span data-ttu-id="778b6-108">**Get-AzCosmosDBMongoDBCollection** Cmdlet은 CosmosDB MongoDB 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="778b6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="778b6-109">EXAMPLES</span></span>

### <span data-ttu-id="778b6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="778b6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="778b6-111">리소스 개체에 MongoIndexes, _rid, _ts _etag 속성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="778b6-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="778b6-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="778b6-113">이 예제에서는 검색 된 컬렉션의 ShardKey를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="778b6-114">변수</span><span class="sxs-lookup"><span data-stu-id="778b6-114">PARAMETERS</span></span>

### <span data-ttu-id="778b6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="778b6-115">-AccountName</span></span>
<span data-ttu-id="778b6-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="778b6-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="778b6-117">-DatabaseName</span></span>
<span data-ttu-id="778b6-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-118">Database name.</span></span>

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

### <span data-ttu-id="778b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778b6-119">-DefaultProfile</span></span>
<span data-ttu-id="778b6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="778b6-121">-이름</span><span class="sxs-lookup"><span data-stu-id="778b6-121">-Name</span></span>
<span data-ttu-id="778b6-122">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-122">Collection name.</span></span>

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

### <span data-ttu-id="778b6-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="778b6-123">-ParentObject</span></span>
<span data-ttu-id="778b6-124">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="778b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="778b6-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-126">Name of resource group.</span></span>

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

### <span data-ttu-id="778b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778b6-127">CommonParameters</span></span>
<span data-ttu-id="778b6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="778b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778b6-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="778b6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778b6-130">입력</span><span class="sxs-lookup"><span data-stu-id="778b6-130">INPUTS</span></span>

### <span data-ttu-id="778b6-131">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="778b6-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="778b6-132">출력</span><span class="sxs-lookup"><span data-stu-id="778b6-132">OUTPUTS</span></span>

### <span data-ttu-id="778b6-133">CosmosDB. PSMongoDBCollectionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="778b6-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="778b6-134">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="778b6-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="778b6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="778b6-135">NOTES</span></span>

## <span data-ttu-id="778b6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="778b6-136">RELATED LINKS</span></span>
