---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493734"
---
# <span data-ttu-id="5c7a1-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="5c7a1-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="5c7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7a1-103">CosmosDB Gremlin Graph의 진행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5c7a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c7a1-104">SYNTAX</span></span>

### <span data-ttu-id="5c7a1-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c7a1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c7a1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c7a1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c7a1-107">설명</span><span class="sxs-lookup"><span data-stu-id="5c7a1-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7a1-108">**Get-AzCosmosDBGremlinGraphThroughput** cmdlet은 CosmosDB Gremlin Graph의 삭제를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5c7a1-109">예제</span><span class="sxs-lookup"><span data-stu-id="5c7a1-109">EXAMPLES</span></span>

### <span data-ttu-id="5c7a1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c7a1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="5c7a1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c7a1-111">PARAMETERS</span></span>

### <span data-ttu-id="5c7a1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c7a1-112">-AccountName</span></span>
<span data-ttu-id="5c7a1-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5c7a1-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c7a1-114">-Confirm</span></span>
<span data-ttu-id="5c7a1-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c7a1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c7a1-116">-DatabaseName</span></span>
<span data-ttu-id="5c7a1-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-117">Database name.</span></span>

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

### <span data-ttu-id="5c7a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7a1-118">-DefaultProfile</span></span>
<span data-ttu-id="5c7a1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c7a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c7a1-120">-InputObject</span></span>
<span data-ttu-id="5c7a1-121">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="5c7a1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5c7a1-122">-Name</span></span>
<span data-ttu-id="5c7a1-123">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5c7a1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7a1-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c7a1-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5c7a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c7a1-126">-WhatIf</span></span>
<span data-ttu-id="5c7a1-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c7a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c7a1-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c7a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7a1-129">CommonParameters</span></span>
<span data-ttu-id="5c7a1-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7a1-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c7a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7a1-132">입력</span><span class="sxs-lookup"><span data-stu-id="5c7a1-132">INPUTS</span></span>

### <span data-ttu-id="5c7a1-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="5c7a1-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="5c7a1-134">출력</span><span class="sxs-lookup"><span data-stu-id="5c7a1-134">OUTPUTS</span></span>

### <span data-ttu-id="5c7a1-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5c7a1-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5c7a1-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c7a1-136">NOTES</span></span>

## <span data-ttu-id="5c7a1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c7a1-137">RELATED LINKS</span></span>
