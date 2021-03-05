---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: f5357e23b8a4e4ec5c613dc7a6b1b0f53e5bac3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983616"
---
# <span data-ttu-id="65303-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="65303-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="65303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65303-102">SYNOPSIS</span></span>
<span data-ttu-id="65303-103">CosmosDB Gremlin Graph의 진행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65303-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="65303-104">구문</span><span class="sxs-lookup"><span data-stu-id="65303-104">SYNTAX</span></span>

### <span data-ttu-id="65303-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="65303-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65303-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65303-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65303-107">설명</span><span class="sxs-lookup"><span data-stu-id="65303-107">DESCRIPTION</span></span>
<span data-ttu-id="65303-108">**Get-AzCosmosDBGremlinGraphThroughput** cmdlet은 CosmosDB Gremlin Graph의 프로비전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65303-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="65303-109">예제</span><span class="sxs-lookup"><span data-stu-id="65303-109">EXAMPLES</span></span>

### <span data-ttu-id="65303-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="65303-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="65303-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65303-111">PARAMETERS</span></span>

### <span data-ttu-id="65303-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65303-112">-AccountName</span></span>
<span data-ttu-id="65303-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65303-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65303-114">-확인</span><span class="sxs-lookup"><span data-stu-id="65303-114">-Confirm</span></span>
<span data-ttu-id="65303-115">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65303-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65303-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65303-116">-DatabaseName</span></span>
<span data-ttu-id="65303-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65303-117">Database name.</span></span>

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

### <span data-ttu-id="65303-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65303-118">-DefaultProfile</span></span>
<span data-ttu-id="65303-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65303-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65303-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65303-120">-InputObject</span></span>
<span data-ttu-id="65303-121">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="65303-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65303-122">-Name</span><span class="sxs-lookup"><span data-stu-id="65303-122">-Name</span></span>
<span data-ttu-id="65303-123">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65303-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="65303-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65303-124">-ResourceGroupName</span></span>
<span data-ttu-id="65303-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65303-125">Name of resource group.</span></span>

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

### <span data-ttu-id="65303-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65303-126">-WhatIf</span></span>
<span data-ttu-id="65303-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65303-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65303-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65303-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65303-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65303-129">CommonParameters</span></span>
<span data-ttu-id="65303-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65303-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65303-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65303-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65303-132">입력</span><span class="sxs-lookup"><span data-stu-id="65303-132">INPUTS</span></span>

### <span data-ttu-id="65303-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="65303-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="65303-134">출력</span><span class="sxs-lookup"><span data-stu-id="65303-134">OUTPUTS</span></span>

### <span data-ttu-id="65303-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="65303-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="65303-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65303-136">NOTES</span></span>

## <span data-ttu-id="65303-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65303-137">RELATED LINKS</span></span>
