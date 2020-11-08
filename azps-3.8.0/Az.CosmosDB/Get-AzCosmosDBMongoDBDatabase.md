---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: f1cb4a45a68758dc1209b4e30d352def8e348e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044106"
---
# <span data-ttu-id="eb2ca-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="eb2ca-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="eb2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2ca-103">CosmosDB MongoDB 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="eb2ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb2ca-104">SYNTAX</span></span>

### <span data-ttu-id="eb2ca-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb2ca-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb2ca-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb2ca-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb2ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eb2ca-107">DESCRIPTION</span></span>
<span data-ttu-id="eb2ca-108">**Get-AzCosmosDBMongoDBDatabase** Cmdlet은 CosmosDB MongoDB 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="eb2ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eb2ca-109">EXAMPLES</span></span>

### <span data-ttu-id="eb2ca-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="eb2ca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="eb2ca-111">리소스 개체에 _rid, _ts _etag 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="eb2ca-112">변수</span><span class="sxs-lookup"><span data-stu-id="eb2ca-112">PARAMETERS</span></span>

### <span data-ttu-id="eb2ca-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb2ca-113">-AccountName</span></span>
<span data-ttu-id="eb2ca-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eb2ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2ca-115">-DefaultProfile</span></span>
<span data-ttu-id="eb2ca-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb2ca-117">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="eb2ca-117">-Detailed</span></span>
<span data-ttu-id="eb2ca-118">그런 다음 cmdlet은 해당 처리 값을 사용 하 여 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-118">If provided then, the cmdlet returns the database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="eb2ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb2ca-119">-InputObject</span></span>
<span data-ttu-id="eb2ca-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="eb2ca-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb2ca-121">-이름</span><span class="sxs-lookup"><span data-stu-id="eb2ca-121">-Name</span></span>
<span data-ttu-id="eb2ca-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-122">Database name.</span></span>

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

### <span data-ttu-id="eb2ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb2ca-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-124">Name of resource group.</span></span>

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

### <span data-ttu-id="eb2ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2ca-125">CommonParameters</span></span>
<span data-ttu-id="eb2ca-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2ca-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2ca-128">입력</span><span class="sxs-lookup"><span data-stu-id="eb2ca-128">INPUTS</span></span>

### <span data-ttu-id="eb2ca-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="eb2ca-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="eb2ca-130">출력</span><span class="sxs-lookup"><span data-stu-id="eb2ca-130">OUTPUTS</span></span>

### <span data-ttu-id="eb2ca-131">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="eb2ca-132">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="eb2ca-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="eb2ca-133">상속자</span><span class="sxs-lookup"><span data-stu-id="eb2ca-133">NOTES</span></span>

## <span data-ttu-id="eb2ca-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb2ca-134">RELATED LINKS</span></span>
