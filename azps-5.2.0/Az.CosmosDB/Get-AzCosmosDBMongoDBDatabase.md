---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322251"
---
# <span data-ttu-id="7199f-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="7199f-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="7199f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7199f-102">SYNOPSIS</span></span>
<span data-ttu-id="7199f-103">CosmosDB MongoDB 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="7199f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7199f-104">SYNTAX</span></span>

### <span data-ttu-id="7199f-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7199f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7199f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7199f-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7199f-107">설명</span><span class="sxs-lookup"><span data-stu-id="7199f-107">DESCRIPTION</span></span>
<span data-ttu-id="7199f-108">**Get-AzCosmosDBMongoDBDatabase** cmdlet은 CosmosDB MongoDB 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="7199f-109">예제</span><span class="sxs-lookup"><span data-stu-id="7199f-109">EXAMPLES</span></span>

### <span data-ttu-id="7199f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7199f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="7199f-111">리소스 개체에는 _rid, _ts _etag 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="7199f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7199f-112">PARAMETERS</span></span>

### <span data-ttu-id="7199f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7199f-113">-AccountName</span></span>
<span data-ttu-id="7199f-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7199f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7199f-115">-DefaultProfile</span></span>
<span data-ttu-id="7199f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7199f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7199f-117">-Name</span></span>
<span data-ttu-id="7199f-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-118">Database name.</span></span>

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

### <span data-ttu-id="7199f-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7199f-119">-ParentObject</span></span>
<span data-ttu-id="7199f-120">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="7199f-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7199f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7199f-121">-ResourceGroupName</span></span>
<span data-ttu-id="7199f-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-122">Name of resource group.</span></span>

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

### <span data-ttu-id="7199f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7199f-123">CommonParameters</span></span>
<span data-ttu-id="7199f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7199f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7199f-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7199f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7199f-126">입력</span><span class="sxs-lookup"><span data-stu-id="7199f-126">INPUTS</span></span>

### <span data-ttu-id="7199f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7199f-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7199f-128">출력</span><span class="sxs-lookup"><span data-stu-id="7199f-128">OUTPUTS</span></span>

### <span data-ttu-id="7199f-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7199f-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="7199f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7199f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7199f-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7199f-131">NOTES</span></span>

## <span data-ttu-id="7199f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7199f-132">RELATED LINKS</span></span>
