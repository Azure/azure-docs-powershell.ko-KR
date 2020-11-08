---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044125"
---
# <span data-ttu-id="95267-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="95267-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="95267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95267-102">SYNOPSIS</span></span>
<span data-ttu-id="95267-103">CosmosDB Gremlin 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95267-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="95267-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95267-104">SYNTAX</span></span>

### <span data-ttu-id="95267-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="95267-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95267-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95267-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95267-107">설명은</span><span class="sxs-lookup"><span data-stu-id="95267-107">DESCRIPTION</span></span>
<span data-ttu-id="95267-108">**Get-AzCosmosDBGremlinDatabase** Cmdlet은 CosmosDB Gremlin 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95267-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="95267-109">예제의</span><span class="sxs-lookup"><span data-stu-id="95267-109">EXAMPLES</span></span>

### <span data-ttu-id="95267-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="95267-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="95267-111">리소스 개체에 _rid, _ts _etag 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95267-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="95267-112">변수</span><span class="sxs-lookup"><span data-stu-id="95267-112">PARAMETERS</span></span>

### <span data-ttu-id="95267-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95267-113">-AccountName</span></span>
<span data-ttu-id="95267-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95267-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="95267-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95267-115">-DefaultProfile</span></span>
<span data-ttu-id="95267-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95267-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95267-117">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="95267-117">-Detailed</span></span>
<span data-ttu-id="95267-118">그런 다음 cmdlet은 해당 처리 값을 사용 하 여 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="95267-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="95267-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95267-119">-InputObject</span></span>
<span data-ttu-id="95267-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="95267-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="95267-121">-이름</span><span class="sxs-lookup"><span data-stu-id="95267-121">-Name</span></span>
<span data-ttu-id="95267-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95267-122">Database name.</span></span>

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

### <span data-ttu-id="95267-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95267-123">-ResourceGroupName</span></span>
<span data-ttu-id="95267-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95267-124">Name of resource group.</span></span>

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

### <span data-ttu-id="95267-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95267-125">CommonParameters</span></span>
<span data-ttu-id="95267-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95267-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95267-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="95267-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95267-128">입력</span><span class="sxs-lookup"><span data-stu-id="95267-128">INPUTS</span></span>

### <span data-ttu-id="95267-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="95267-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="95267-130">출력</span><span class="sxs-lookup"><span data-stu-id="95267-130">OUTPUTS</span></span>

### <span data-ttu-id="95267-131">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="95267-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="95267-132">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="95267-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="95267-133">상속자</span><span class="sxs-lookup"><span data-stu-id="95267-133">NOTES</span></span>

## <span data-ttu-id="95267-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95267-134">RELATED LINKS</span></span>
