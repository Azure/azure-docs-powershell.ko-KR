---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: bb73bd88abf677f9855d934a995f3f9107e44b4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978731"
---
# <span data-ttu-id="15f5d-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="15f5d-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="15f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="15f5d-103">CosmosDB MongoDB 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="15f5d-104">구문</span><span class="sxs-lookup"><span data-stu-id="15f5d-104">SYNTAX</span></span>

### <span data-ttu-id="15f5d-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="15f5d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="15f5d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15f5d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15f5d-107">설명</span><span class="sxs-lookup"><span data-stu-id="15f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="15f5d-108">**Get-AzCosmosDBMongoDBCollection** cmdlet은 CosmosDB MongoDB 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="15f5d-109">예제</span><span class="sxs-lookup"><span data-stu-id="15f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="15f5d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="15f5d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="15f5d-111">리소스 개체에는 MongoIndexes, _rid, _ts _etag 속성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="15f5d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="15f5d-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="15f5d-113">이 예제에서는 검색된 컬렉션의 ShardKey를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="15f5d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="15f5d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15f5d-115">-AccountName</span></span>
<span data-ttu-id="15f5d-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="15f5d-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15f5d-117">-DatabaseName</span></span>
<span data-ttu-id="15f5d-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-118">Database name.</span></span>

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

### <span data-ttu-id="15f5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f5d-119">-DefaultProfile</span></span>
<span data-ttu-id="15f5d-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15f5d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="15f5d-121">-Name</span></span>
<span data-ttu-id="15f5d-122">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-122">Collection name.</span></span>

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

### <span data-ttu-id="15f5d-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15f5d-123">-ParentObject</span></span>
<span data-ttu-id="15f5d-124">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="15f5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="15f5d-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-126">Name of resource group.</span></span>

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

### <span data-ttu-id="15f5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f5d-127">CommonParameters</span></span>
<span data-ttu-id="15f5d-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15f5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f5d-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15f5d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f5d-130">입력</span><span class="sxs-lookup"><span data-stu-id="15f5d-130">INPUTS</span></span>

### <span data-ttu-id="15f5d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="15f5d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="15f5d-132">출력</span><span class="sxs-lookup"><span data-stu-id="15f5d-132">OUTPUTS</span></span>

### <span data-ttu-id="15f5d-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="15f5d-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="15f5d-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="15f5d-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="15f5d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15f5d-135">NOTES</span></span>

## <span data-ttu-id="15f5d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15f5d-136">RELATED LINKS</span></span>
