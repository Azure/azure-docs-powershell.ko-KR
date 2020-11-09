---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307295"
---
# <span data-ttu-id="08599-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="08599-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="08599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08599-102">SYNOPSIS</span></span>
<span data-ttu-id="08599-103">CosmosDB Gremlin Graph의 처리량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08599-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="08599-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08599-104">SYNTAX</span></span>

### <span data-ttu-id="08599-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="08599-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08599-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08599-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08599-107">설명은</span><span class="sxs-lookup"><span data-stu-id="08599-107">DESCRIPTION</span></span>
<span data-ttu-id="08599-108">**AzCosmosDBGremlinGraphThroughput** Cmdlet은 CosmosDB Gremlin Graph의 처리량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08599-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="08599-109">예제의</span><span class="sxs-lookup"><span data-stu-id="08599-109">EXAMPLES</span></span>

### <span data-ttu-id="08599-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="08599-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="08599-111">변수</span><span class="sxs-lookup"><span data-stu-id="08599-111">PARAMETERS</span></span>

### <span data-ttu-id="08599-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08599-112">-AccountName</span></span>
<span data-ttu-id="08599-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08599-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="08599-114">-확인</span><span class="sxs-lookup"><span data-stu-id="08599-114">-Confirm</span></span>
<span data-ttu-id="08599-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08599-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08599-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08599-116">-DatabaseName</span></span>
<span data-ttu-id="08599-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08599-117">Database name.</span></span>

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

### <span data-ttu-id="08599-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08599-118">-DefaultProfile</span></span>
<span data-ttu-id="08599-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08599-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08599-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08599-120">-InputObject</span></span>
<span data-ttu-id="08599-121">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08599-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="08599-122">-이름</span><span class="sxs-lookup"><span data-stu-id="08599-122">-Name</span></span>
<span data-ttu-id="08599-123">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08599-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="08599-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08599-124">-ResourceGroupName</span></span>
<span data-ttu-id="08599-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08599-125">Name of resource group.</span></span>

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

### <span data-ttu-id="08599-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08599-126">-WhatIf</span></span>
<span data-ttu-id="08599-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08599-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08599-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08599-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08599-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08599-129">CommonParameters</span></span>
<span data-ttu-id="08599-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08599-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08599-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08599-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08599-132">입력</span><span class="sxs-lookup"><span data-stu-id="08599-132">INPUTS</span></span>

### <span data-ttu-id="08599-133">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="08599-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="08599-134">출력</span><span class="sxs-lookup"><span data-stu-id="08599-134">OUTPUTS</span></span>

### <span data-ttu-id="08599-135">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="08599-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="08599-136">상속자</span><span class="sxs-lookup"><span data-stu-id="08599-136">NOTES</span></span>

## <span data-ttu-id="08599-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08599-137">RELATED LINKS</span></span>
