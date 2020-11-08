---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042183"
---
# <span data-ttu-id="f5ab4-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="f5ab4-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="f5ab4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ab4-103">CosmosDB Gremlin Graph의 처리 속도 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="f5ab4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5ab4-104">SYNTAX</span></span>

### <span data-ttu-id="f5ab4-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5ab4-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ab4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5ab4-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5ab4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5ab4-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5ab4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f5ab4-108">EXAMPLES</span></span>

### <span data-ttu-id="f5ab4-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5ab4-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="f5ab4-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5ab4-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ab4-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5ab4-111">-AccountName</span></span>
<span data-ttu-id="f5ab4-112">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f5ab4-113">-확인</span><span class="sxs-lookup"><span data-stu-id="f5ab4-113">-Confirm</span></span>
<span data-ttu-id="f5ab4-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5ab4-115">-DatabaseName</span></span>
<span data-ttu-id="f5ab4-116">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-116">Database name.</span></span>

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

### <span data-ttu-id="f5ab4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ab4-117">-DefaultProfile</span></span>
<span data-ttu-id="f5ab4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ab4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5ab4-119">-InputObject</span></span>
<span data-ttu-id="f5ab4-120">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f5ab4-121">-Name</span></span>
<span data-ttu-id="f5ab4-122">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="f5ab4-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f5ab4-123">-ParentObject</span></span>
<span data-ttu-id="f5ab4-124">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ab4-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5ab4-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f5ab4-127">-처리량</span><span class="sxs-lookup"><span data-stu-id="f5ab4-127">-Throughput</span></span>
<span data-ttu-id="f5ab4-128">Gremlin 그래프의 처리량 (1/s)</span><span class="sxs-lookup"><span data-stu-id="f5ab4-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="f5ab4-129">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ab4-130">-WhatIf</span></span>
<span data-ttu-id="f5ab4-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ab4-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ab4-133">CommonParameters</span></span>
<span data-ttu-id="f5ab4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ab4-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ab4-136">입력</span><span class="sxs-lookup"><span data-stu-id="f5ab4-136">INPUTS</span></span>

### <span data-ttu-id="f5ab4-137">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f5ab4-138">출력</span><span class="sxs-lookup"><span data-stu-id="f5ab4-138">OUTPUTS</span></span>

### <span data-ttu-id="f5ab4-139">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="f5ab4-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f5ab4-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f5ab4-140">NOTES</span></span>

## <span data-ttu-id="f5ab4-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5ab4-141">RELATED LINKS</span></span>
