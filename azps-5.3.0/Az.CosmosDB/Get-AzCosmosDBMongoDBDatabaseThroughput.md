---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493728"
---
# <span data-ttu-id="ab5b4-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ab5b4-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="ab5b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5b4-103">MongoDB 데이터베이스의 CosmosDB 데이터당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="ab5b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab5b4-104">SYNTAX</span></span>

### <span data-ttu-id="ab5b4-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab5b4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab5b4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab5b4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab5b4-107">설명</span><span class="sxs-lookup"><span data-stu-id="ab5b4-107">DESCRIPTION</span></span>
<span data-ttu-id="ab5b4-108">**Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet은 MongoDB 데이터베이스의 프로시저 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="ab5b4-109">예제</span><span class="sxs-lookup"><span data-stu-id="ab5b4-109">EXAMPLES</span></span>

### <span data-ttu-id="ab5b4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab5b4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ab5b4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab5b4-111">PARAMETERS</span></span>

### <span data-ttu-id="ab5b4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ab5b4-112">-AccountName</span></span>
<span data-ttu-id="ab5b4-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ab5b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab5b4-114">-DefaultProfile</span></span>
<span data-ttu-id="ab5b4-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab5b4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab5b4-116">-InputObject</span></span>
<span data-ttu-id="ab5b4-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ab5b4-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ab5b4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ab5b4-118">-Name</span></span>
<span data-ttu-id="ab5b4-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-119">Database name.</span></span>

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

### <span data-ttu-id="ab5b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="ab5b4-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ab5b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5b4-122">CommonParameters</span></span>
<span data-ttu-id="ab5b4-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5b4-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab5b4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5b4-125">입력</span><span class="sxs-lookup"><span data-stu-id="ab5b4-125">INPUTS</span></span>

### <span data-ttu-id="ab5b4-126">없음</span><span class="sxs-lookup"><span data-stu-id="ab5b4-126">None</span></span>

## <span data-ttu-id="ab5b4-127">출력</span><span class="sxs-lookup"><span data-stu-id="ab5b4-127">OUTPUTS</span></span>

### <span data-ttu-id="ab5b4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ab5b4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ab5b4-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab5b4-129">NOTES</span></span>

## <span data-ttu-id="ab5b4-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab5b4-130">RELATED LINKS</span></span>
