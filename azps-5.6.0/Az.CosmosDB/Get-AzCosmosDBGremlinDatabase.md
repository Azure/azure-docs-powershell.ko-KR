---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 7268eff2163e408975b1711dcac4fbf8454f0b76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004368"
---
# <span data-ttu-id="ce98b-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="ce98b-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="ce98b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce98b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce98b-103">CosmosDB Gremlin Database를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ce98b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce98b-104">SYNTAX</span></span>

### <span data-ttu-id="ce98b-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce98b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce98b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce98b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce98b-107">설명</span><span class="sxs-lookup"><span data-stu-id="ce98b-107">DESCRIPTION</span></span>
<span data-ttu-id="ce98b-108">**Get-AzCosmosDBGremlinDatabase** cmdlet은 CosmosDB Gremlin Database를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ce98b-109">예제</span><span class="sxs-lookup"><span data-stu-id="ce98b-109">EXAMPLES</span></span>

### <span data-ttu-id="ce98b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce98b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="ce98b-111">리소스 개체에는 _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="ce98b-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="ce98b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce98b-112">PARAMETERS</span></span>

### <span data-ttu-id="ce98b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ce98b-113">-AccountName</span></span>
<span data-ttu-id="ce98b-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ce98b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce98b-115">-DefaultProfile</span></span>
<span data-ttu-id="ce98b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce98b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ce98b-117">-Name</span></span>
<span data-ttu-id="ce98b-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-118">Database name.</span></span>

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

### <span data-ttu-id="ce98b-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ce98b-119">-ParentObject</span></span>
<span data-ttu-id="ce98b-120">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ce98b-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ce98b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce98b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce98b-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-122">Name of resource group.</span></span>

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

### <span data-ttu-id="ce98b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce98b-123">CommonParameters</span></span>
<span data-ttu-id="ce98b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce98b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce98b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce98b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce98b-126">입력</span><span class="sxs-lookup"><span data-stu-id="ce98b-126">INPUTS</span></span>

### <span data-ttu-id="ce98b-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ce98b-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ce98b-128">출력</span><span class="sxs-lookup"><span data-stu-id="ce98b-128">OUTPUTS</span></span>

### <span data-ttu-id="ce98b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ce98b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="ce98b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ce98b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ce98b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce98b-131">NOTES</span></span>

## <span data-ttu-id="ce98b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce98b-132">RELATED LINKS</span></span>
