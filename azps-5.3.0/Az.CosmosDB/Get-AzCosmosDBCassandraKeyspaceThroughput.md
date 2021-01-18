---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493740"
---
# <span data-ttu-id="87bae-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="87bae-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="87bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87bae-102">SYNOPSIS</span></span>
<span data-ttu-id="87bae-103">Cassandra Keyspace의 사용료 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="87bae-104">구문</span><span class="sxs-lookup"><span data-stu-id="87bae-104">SYNTAX</span></span>

### <span data-ttu-id="87bae-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="87bae-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87bae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87bae-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87bae-107">설명</span><span class="sxs-lookup"><span data-stu-id="87bae-107">DESCRIPTION</span></span>
<span data-ttu-id="87bae-108">**Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet은 주어진 Keyspace에 해당하는 처리물 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="87bae-109">예제</span><span class="sxs-lookup"><span data-stu-id="87bae-109">EXAMPLES</span></span>

### <span data-ttu-id="87bae-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="87bae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="87bae-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87bae-111">PARAMETERS</span></span>

### <span data-ttu-id="87bae-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="87bae-112">-AccountName</span></span>
<span data-ttu-id="87bae-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="87bae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bae-114">-DefaultProfile</span></span>
<span data-ttu-id="87bae-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87bae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87bae-116">-InputObject</span></span>
<span data-ttu-id="87bae-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="87bae-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="87bae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="87bae-118">-Name</span></span>
<span data-ttu-id="87bae-119">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="87bae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87bae-120">-ResourceGroupName</span></span>
<span data-ttu-id="87bae-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-121">Name of resource group.</span></span>

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

### <span data-ttu-id="87bae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bae-122">CommonParameters</span></span>
<span data-ttu-id="87bae-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87bae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bae-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87bae-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bae-125">입력</span><span class="sxs-lookup"><span data-stu-id="87bae-125">INPUTS</span></span>

### <span data-ttu-id="87bae-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="87bae-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="87bae-127">출력</span><span class="sxs-lookup"><span data-stu-id="87bae-127">OUTPUTS</span></span>

### <span data-ttu-id="87bae-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="87bae-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="87bae-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87bae-129">NOTES</span></span>

## <span data-ttu-id="87bae-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87bae-130">RELATED LINKS</span></span>
