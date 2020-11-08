---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215076"
---
# <span data-ttu-id="280db-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="280db-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="280db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="280db-102">SYNOPSIS</span></span>
<span data-ttu-id="280db-103">CosmosDB Gremlin Graph의 처리 속도 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="280db-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="280db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="280db-104">SYNTAX</span></span>

### <span data-ttu-id="280db-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="280db-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="280db-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="280db-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="280db-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="280db-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="280db-108">설명은</span><span class="sxs-lookup"><span data-stu-id="280db-108">DESCRIPTION</span></span>
<span data-ttu-id="280db-109">CosmosDB Gremlin Graph의 처리 속도 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="280db-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="280db-110">예제의</span><span class="sxs-lookup"><span data-stu-id="280db-110">EXAMPLES</span></span>

### <span data-ttu-id="280db-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="280db-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="280db-112">변수</span><span class="sxs-lookup"><span data-stu-id="280db-112">PARAMETERS</span></span>

### <span data-ttu-id="280db-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="280db-113">-AccountName</span></span>
<span data-ttu-id="280db-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="280db-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="280db-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="280db-116">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280db-117">-확인</span><span class="sxs-lookup"><span data-stu-id="280db-117">-Confirm</span></span>
<span data-ttu-id="280db-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="280db-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="280db-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="280db-119">-DatabaseName</span></span>
<span data-ttu-id="280db-120">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-120">Database name.</span></span>

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

### <span data-ttu-id="280db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280db-121">-DefaultProfile</span></span>
<span data-ttu-id="280db-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="280db-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="280db-123">-InputObject</span></span>
<span data-ttu-id="280db-124">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="280db-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="280db-125">-이름</span><span class="sxs-lookup"><span data-stu-id="280db-125">-Name</span></span>
<span data-ttu-id="280db-126">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="280db-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="280db-127">-ParentObject</span></span>
<span data-ttu-id="280db-128">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="280db-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="280db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="280db-129">-ResourceGroupName</span></span>
<span data-ttu-id="280db-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-130">Name of resource group.</span></span>

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

### <span data-ttu-id="280db-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="280db-131">-Throughput</span></span>
<span data-ttu-id="280db-132">Gremlin 그래프의 처리량 (1/s)</span><span class="sxs-lookup"><span data-stu-id="280db-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="280db-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="280db-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="280db-134">-WhatIf</span></span>
<span data-ttu-id="280db-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="280db-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="280db-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="280db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="280db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280db-137">CommonParameters</span></span>
<span data-ttu-id="280db-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="280db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280db-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="280db-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280db-140">입력</span><span class="sxs-lookup"><span data-stu-id="280db-140">INPUTS</span></span>

### <span data-ttu-id="280db-141">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="280db-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="280db-142">출력</span><span class="sxs-lookup"><span data-stu-id="280db-142">OUTPUTS</span></span>

### <span data-ttu-id="280db-143">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="280db-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="280db-144">상속자</span><span class="sxs-lookup"><span data-stu-id="280db-144">NOTES</span></span>

## <span data-ttu-id="280db-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="280db-145">RELATED LINKS</span></span>
