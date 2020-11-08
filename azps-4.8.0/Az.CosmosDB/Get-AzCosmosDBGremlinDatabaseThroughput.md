---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056479"
---
# <span data-ttu-id="6b1d9-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="6b1d9-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="6b1d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1d9-103">CosmosDB Gremlin 데이터베이스의 처리량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="6b1d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b1d9-104">SYNTAX</span></span>

### <span data-ttu-id="6b1d9-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b1d9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b1d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b1d9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b1d9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6b1d9-107">DESCRIPTION</span></span>
<span data-ttu-id="6b1d9-108">**AzCosmosDBGremlinDatabaseThroughput** Cmdlet은 CosmosDB Gremlin 데이터베이스의 처리량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="6b1d9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6b1d9-109">EXAMPLES</span></span>

### <span data-ttu-id="6b1d9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b1d9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="6b1d9-111">변수</span><span class="sxs-lookup"><span data-stu-id="6b1d9-111">PARAMETERS</span></span>

### <span data-ttu-id="6b1d9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6b1d9-112">-AccountName</span></span>
<span data-ttu-id="6b1d9-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6b1d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1d9-114">-DefaultProfile</span></span>
<span data-ttu-id="6b1d9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b1d9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b1d9-116">-InputObject</span></span>
<span data-ttu-id="6b1d9-117">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="6b1d9-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1d9-118">-이름</span><span class="sxs-lookup"><span data-stu-id="6b1d9-118">-Name</span></span>
<span data-ttu-id="6b1d9-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-119">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b1d9-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-121">Name of resource group.</span></span>

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

### <span data-ttu-id="6b1d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1d9-122">CommonParameters</span></span>
<span data-ttu-id="6b1d9-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1d9-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1d9-125">입력</span><span class="sxs-lookup"><span data-stu-id="6b1d9-125">INPUTS</span></span>

### <span data-ttu-id="6b1d9-126">않아야</span><span class="sxs-lookup"><span data-stu-id="6b1d9-126">None</span></span>

## <span data-ttu-id="6b1d9-127">출력</span><span class="sxs-lookup"><span data-stu-id="6b1d9-127">OUTPUTS</span></span>

### <span data-ttu-id="6b1d9-128">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="6b1d9-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6b1d9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="6b1d9-129">NOTES</span></span>

## <span data-ttu-id="6b1d9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b1d9-130">RELATED LINKS</span></span>
