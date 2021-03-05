---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 965e7b3d1f0775f3842e423e47c1a4cc60021408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983723"
---
# <span data-ttu-id="56336-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="56336-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="56336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56336-102">SYNOPSIS</span></span>
<span data-ttu-id="56336-103">Cassandra Keyspace의 작업당 값입니다.</span><span class="sxs-lookup"><span data-stu-id="56336-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="56336-104">구문</span><span class="sxs-lookup"><span data-stu-id="56336-104">SYNTAX</span></span>

### <span data-ttu-id="56336-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="56336-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56336-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56336-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56336-107">설명</span><span class="sxs-lookup"><span data-stu-id="56336-107">DESCRIPTION</span></span>
<span data-ttu-id="56336-108">**Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet은 주어진 키스페이스에 해당하는 처리물 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56336-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="56336-109">예제</span><span class="sxs-lookup"><span data-stu-id="56336-109">EXAMPLES</span></span>

### <span data-ttu-id="56336-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="56336-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="56336-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56336-111">PARAMETERS</span></span>

### <span data-ttu-id="56336-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56336-112">-AccountName</span></span>
<span data-ttu-id="56336-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56336-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="56336-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56336-114">-DefaultProfile</span></span>
<span data-ttu-id="56336-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56336-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56336-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56336-116">-InputObject</span></span>
<span data-ttu-id="56336-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="56336-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="56336-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56336-118">-Name</span></span>
<span data-ttu-id="56336-119">Cassandra 키스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56336-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="56336-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56336-120">-ResourceGroupName</span></span>
<span data-ttu-id="56336-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56336-121">Name of resource group.</span></span>

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

### <span data-ttu-id="56336-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56336-122">CommonParameters</span></span>
<span data-ttu-id="56336-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56336-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56336-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56336-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56336-125">입력</span><span class="sxs-lookup"><span data-stu-id="56336-125">INPUTS</span></span>

### <span data-ttu-id="56336-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="56336-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="56336-127">출력</span><span class="sxs-lookup"><span data-stu-id="56336-127">OUTPUTS</span></span>

### <span data-ttu-id="56336-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="56336-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="56336-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56336-129">NOTES</span></span>

## <span data-ttu-id="56336-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56336-130">RELATED LINKS</span></span>
