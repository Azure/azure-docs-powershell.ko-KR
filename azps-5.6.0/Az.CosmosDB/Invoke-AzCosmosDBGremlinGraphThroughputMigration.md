---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 4fc0c28293484b2f3791145591576d4110ac2974
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990341"
---
# <span data-ttu-id="1d9cd-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="1d9cd-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="1d9cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9cd-103">이 방법을 사용하여 자동 조정된 작업량은 수동 작업량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="1d9cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d9cd-104">SYNTAX</span></span>

### <span data-ttu-id="1d9cd-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d9cd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d9cd-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d9cd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d9cd-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d9cd-108">설명</span><span class="sxs-lookup"><span data-stu-id="1d9cd-108">DESCRIPTION</span></span>
<span data-ttu-id="1d9cd-109">ThroughpyteType paramter는 마이그레이션할 수 있는 이루어 를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="1d9cd-110">예제</span><span class="sxs-lookup"><span data-stu-id="1d9cd-110">EXAMPLES</span></span>

### <span data-ttu-id="1d9cd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d9cd-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="1d9cd-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d9cd-112">PARAMETERS</span></span>

### <span data-ttu-id="1d9cd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d9cd-113">-AccountName</span></span>
<span data-ttu-id="1d9cd-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d9cd-115">-확인</span><span class="sxs-lookup"><span data-stu-id="1d9cd-115">-Confirm</span></span>
<span data-ttu-id="1d9cd-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d9cd-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d9cd-117">-DatabaseName</span></span>
<span data-ttu-id="1d9cd-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-118">Database name.</span></span>

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

### <span data-ttu-id="1d9cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9cd-119">-DefaultProfile</span></span>
<span data-ttu-id="1d9cd-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d9cd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d9cd-121">-InputObject</span></span>
<span data-ttu-id="1d9cd-122">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="1d9cd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1d9cd-123">-Name</span></span>
<span data-ttu-id="1d9cd-124">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1d9cd-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d9cd-125">-ParentObject</span></span>
<span data-ttu-id="1d9cd-126">Gremlin Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="1d9cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d9cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d9cd-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-128">Name of resource group.</span></span>

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

### <span data-ttu-id="1d9cd-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="1d9cd-129">-ThroughputType</span></span>
<span data-ttu-id="1d9cd-130">마이그레이션할 수 있는 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="1d9cd-131">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="1d9cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d9cd-132">-WhatIf</span></span>
<span data-ttu-id="1d9cd-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d9cd-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d9cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9cd-135">CommonParameters</span></span>
<span data-ttu-id="1d9cd-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d9cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9cd-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d9cd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9cd-138">입력</span><span class="sxs-lookup"><span data-stu-id="1d9cd-138">INPUTS</span></span>

### <span data-ttu-id="1d9cd-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1d9cd-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="1d9cd-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1d9cd-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="1d9cd-141">출력</span><span class="sxs-lookup"><span data-stu-id="1d9cd-141">OUTPUTS</span></span>

### <span data-ttu-id="1d9cd-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1d9cd-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1d9cd-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d9cd-143">NOTES</span></span>

## <span data-ttu-id="1d9cd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d9cd-144">RELATED LINKS</span></span>
