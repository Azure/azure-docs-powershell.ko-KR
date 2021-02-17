---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16817d4af40ddd27a8838f40618758686af26a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196857"
---
# <span data-ttu-id="d261a-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d261a-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="d261a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d261a-102">SYNOPSIS</span></span>
<span data-ttu-id="d261a-103">이 기능을 사용하여 자동 조정된 데이터로 자동 조정된 데이터를 수동으로 마이그레이션하거나 그 반대로 마이그레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d261a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d261a-104">SYNTAX</span></span>

### <span data-ttu-id="d261a-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d261a-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d261a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d261a-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d261a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d261a-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d261a-108">설명</span><span class="sxs-lookup"><span data-stu-id="d261a-108">DESCRIPTION</span></span>
<span data-ttu-id="d261a-109">ThroughpyteType paramter는 마이그레이션하려는 데이터 양을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d261a-110">예제</span><span class="sxs-lookup"><span data-stu-id="d261a-110">EXAMPLES</span></span>

### <span data-ttu-id="d261a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d261a-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="d261a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d261a-112">PARAMETERS</span></span>

### <span data-ttu-id="d261a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d261a-113">-AccountName</span></span>
<span data-ttu-id="d261a-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d261a-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d261a-115">-Confirm</span></span>
<span data-ttu-id="d261a-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d261a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d261a-117">-DatabaseName</span></span>
<span data-ttu-id="d261a-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-118">Database name.</span></span>

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

### <span data-ttu-id="d261a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d261a-119">-DefaultProfile</span></span>
<span data-ttu-id="d261a-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d261a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d261a-121">-InputObject</span></span>
<span data-ttu-id="d261a-122">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="d261a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d261a-123">-Name</span></span>
<span data-ttu-id="d261a-124">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d261a-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d261a-125">-ParentObject</span></span>
<span data-ttu-id="d261a-126">Gremlin 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d261a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d261a-127">-ResourceGroupName</span></span>
<span data-ttu-id="d261a-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d261a-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="d261a-129">-ThroughputType</span></span>
<span data-ttu-id="d261a-130">마이그레이션할 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="d261a-131">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d261a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d261a-132">-WhatIf</span></span>
<span data-ttu-id="d261a-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d261a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d261a-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d261a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d261a-135">CommonParameters</span></span>
<span data-ttu-id="d261a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d261a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d261a-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d261a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d261a-138">입력</span><span class="sxs-lookup"><span data-stu-id="d261a-138">INPUTS</span></span>

### <span data-ttu-id="d261a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d261a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="d261a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d261a-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="d261a-141">출력</span><span class="sxs-lookup"><span data-stu-id="d261a-141">OUTPUTS</span></span>

### <span data-ttu-id="d261a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d261a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d261a-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d261a-143">NOTES</span></span>

## <span data-ttu-id="d261a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d261a-144">RELATED LINKS</span></span>
