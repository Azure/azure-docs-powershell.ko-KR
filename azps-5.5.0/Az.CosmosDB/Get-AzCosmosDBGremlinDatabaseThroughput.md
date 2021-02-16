---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199036"
---
# <span data-ttu-id="21ed6-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="21ed6-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="21ed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="21ed6-103">CosmosDB Gremlin 데이터베이스의 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="21ed6-104">구문</span><span class="sxs-lookup"><span data-stu-id="21ed6-104">SYNTAX</span></span>

### <span data-ttu-id="21ed6-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="21ed6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21ed6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ed6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21ed6-107">설명</span><span class="sxs-lookup"><span data-stu-id="21ed6-107">DESCRIPTION</span></span>
<span data-ttu-id="21ed6-108">**Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet은 CosmosDB Gremlin 데이터베이스의 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="21ed6-109">예제</span><span class="sxs-lookup"><span data-stu-id="21ed6-109">EXAMPLES</span></span>

### <span data-ttu-id="21ed6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="21ed6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="21ed6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21ed6-111">PARAMETERS</span></span>

### <span data-ttu-id="21ed6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21ed6-112">-AccountName</span></span>
<span data-ttu-id="21ed6-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="21ed6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ed6-114">-DefaultProfile</span></span>
<span data-ttu-id="21ed6-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21ed6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21ed6-116">-InputObject</span></span>
<span data-ttu-id="21ed6-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="21ed6-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="21ed6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="21ed6-118">-Name</span></span>
<span data-ttu-id="21ed6-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-119">Database name.</span></span>

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

### <span data-ttu-id="21ed6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ed6-120">-ResourceGroupName</span></span>
<span data-ttu-id="21ed6-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-121">Name of resource group.</span></span>

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

### <span data-ttu-id="21ed6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ed6-122">CommonParameters</span></span>
<span data-ttu-id="21ed6-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21ed6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ed6-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21ed6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ed6-125">입력</span><span class="sxs-lookup"><span data-stu-id="21ed6-125">INPUTS</span></span>

### <span data-ttu-id="21ed6-126">없음</span><span class="sxs-lookup"><span data-stu-id="21ed6-126">None</span></span>

## <span data-ttu-id="21ed6-127">출력</span><span class="sxs-lookup"><span data-stu-id="21ed6-127">OUTPUTS</span></span>

### <span data-ttu-id="21ed6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="21ed6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="21ed6-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21ed6-129">NOTES</span></span>

## <span data-ttu-id="21ed6-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21ed6-130">RELATED LINKS</span></span>
