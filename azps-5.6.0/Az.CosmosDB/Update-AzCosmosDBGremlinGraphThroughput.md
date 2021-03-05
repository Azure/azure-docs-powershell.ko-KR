---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: c5d7bc79185639c4ec79ab14d7ed2f6201dcedb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977323"
---
# <span data-ttu-id="594da-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="594da-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="594da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="594da-102">SYNOPSIS</span></span>
<span data-ttu-id="594da-103">CosmosDB Gremlin Graph의 진행 시간 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="594da-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="594da-104">구문</span><span class="sxs-lookup"><span data-stu-id="594da-104">SYNTAX</span></span>

### <span data-ttu-id="594da-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="594da-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594da-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="594da-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="594da-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="594da-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="594da-108">설명</span><span class="sxs-lookup"><span data-stu-id="594da-108">DESCRIPTION</span></span>
<span data-ttu-id="594da-109">CosmosDB Gremlin Graph의 진행 시간 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="594da-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="594da-110">예제</span><span class="sxs-lookup"><span data-stu-id="594da-110">EXAMPLES</span></span>

### <span data-ttu-id="594da-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="594da-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="594da-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="594da-112">PARAMETERS</span></span>

### <span data-ttu-id="594da-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="594da-113">-AccountName</span></span>
<span data-ttu-id="594da-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="594da-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="594da-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="594da-116">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="594da-117">-확인</span><span class="sxs-lookup"><span data-stu-id="594da-117">-Confirm</span></span>
<span data-ttu-id="594da-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="594da-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="594da-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="594da-119">-DatabaseName</span></span>
<span data-ttu-id="594da-120">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-120">Database name.</span></span>

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

### <span data-ttu-id="594da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594da-121">-DefaultProfile</span></span>
<span data-ttu-id="594da-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="594da-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="594da-123">-InputObject</span></span>
<span data-ttu-id="594da-124">Gremlin Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="594da-125">-Name</span><span class="sxs-lookup"><span data-stu-id="594da-125">-Name</span></span>
<span data-ttu-id="594da-126">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="594da-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="594da-127">-ParentObject</span></span>
<span data-ttu-id="594da-128">Gremlin Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="594da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594da-129">-ResourceGroupName</span></span>
<span data-ttu-id="594da-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-130">Name of resource group.</span></span>

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

### <span data-ttu-id="594da-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="594da-131">-Throughput</span></span>
<span data-ttu-id="594da-132">GREmlin Graph(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="594da-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="594da-133">Default value is 400.</span></span>

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

### <span data-ttu-id="594da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="594da-134">-WhatIf</span></span>
<span data-ttu-id="594da-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="594da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="594da-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="594da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="594da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594da-137">CommonParameters</span></span>
<span data-ttu-id="594da-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="594da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594da-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="594da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594da-140">입력</span><span class="sxs-lookup"><span data-stu-id="594da-140">INPUTS</span></span>

### <span data-ttu-id="594da-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="594da-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="594da-142">출력</span><span class="sxs-lookup"><span data-stu-id="594da-142">OUTPUTS</span></span>

### <span data-ttu-id="594da-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="594da-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="594da-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="594da-144">NOTES</span></span>

## <span data-ttu-id="594da-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="594da-145">RELATED LINKS</span></span>
