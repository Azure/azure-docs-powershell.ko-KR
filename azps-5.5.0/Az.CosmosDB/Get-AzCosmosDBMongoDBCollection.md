---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204656"
---
# <span data-ttu-id="affef-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="affef-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="affef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="affef-102">SYNOPSIS</span></span>
<span data-ttu-id="affef-103">CosmosDB MongoDB 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="affef-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="affef-104">구문</span><span class="sxs-lookup"><span data-stu-id="affef-104">SYNTAX</span></span>

### <span data-ttu-id="affef-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="affef-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="affef-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="affef-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="affef-107">설명</span><span class="sxs-lookup"><span data-stu-id="affef-107">DESCRIPTION</span></span>
<span data-ttu-id="affef-108">**Get-AzCosmosDBMongoDBCollection** cmdlet은 CosmosDB MongoDB 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="affef-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="affef-109">예제</span><span class="sxs-lookup"><span data-stu-id="affef-109">EXAMPLES</span></span>

### <span data-ttu-id="affef-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="affef-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="affef-111">리소스 개체에는 MongoIndexes, _rid, _ts _etag 있습니다.</span><span class="sxs-lookup"><span data-stu-id="affef-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="affef-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="affef-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="affef-113">이 예제에서는 검색된 컬렉션의 ShardKey를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="affef-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="affef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="affef-114">PARAMETERS</span></span>

### <span data-ttu-id="affef-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="affef-115">-AccountName</span></span>
<span data-ttu-id="affef-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="affef-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="affef-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="affef-117">-DatabaseName</span></span>
<span data-ttu-id="affef-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="affef-118">Database name.</span></span>

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

### <span data-ttu-id="affef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affef-119">-DefaultProfile</span></span>
<span data-ttu-id="affef-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="affef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="affef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="affef-121">-Name</span></span>
<span data-ttu-id="affef-122">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="affef-122">Collection name.</span></span>

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

### <span data-ttu-id="affef-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="affef-123">-ParentObject</span></span>
<span data-ttu-id="affef-124">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="affef-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="affef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affef-125">-ResourceGroupName</span></span>
<span data-ttu-id="affef-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="affef-126">Name of resource group.</span></span>

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

### <span data-ttu-id="affef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affef-127">CommonParameters</span></span>
<span data-ttu-id="affef-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="affef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affef-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="affef-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affef-130">입력</span><span class="sxs-lookup"><span data-stu-id="affef-130">INPUTS</span></span>

### <span data-ttu-id="affef-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="affef-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="affef-132">출력</span><span class="sxs-lookup"><span data-stu-id="affef-132">OUTPUTS</span></span>

### <span data-ttu-id="affef-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="affef-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="affef-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="affef-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="affef-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="affef-135">NOTES</span></span>

## <span data-ttu-id="affef-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="affef-136">RELATED LINKS</span></span>
