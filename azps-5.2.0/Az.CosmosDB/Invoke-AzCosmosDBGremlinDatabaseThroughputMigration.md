---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322391"
---
# <span data-ttu-id="d3871-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d3871-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="d3871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3871-102">SYNOPSIS</span></span>
<span data-ttu-id="d3871-103">이 기능을 사용하여 자동 조정된 데이터로 자동 조정된 데이터를 수동으로 마이그레이션하거나 그 반대로 마이그레이션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d3871-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3871-104">SYNTAX</span></span>

### <span data-ttu-id="d3871-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3871-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3871-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3871-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3871-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3871-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3871-108">설명</span><span class="sxs-lookup"><span data-stu-id="d3871-108">DESCRIPTION</span></span>
<span data-ttu-id="d3871-109">ThroughpyteType paramter는 마이그레이션하려는 데이터 양을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d3871-110">예제</span><span class="sxs-lookup"><span data-stu-id="d3871-110">EXAMPLES</span></span>

### <span data-ttu-id="d3871-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3871-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="d3871-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3871-112">PARAMETERS</span></span>

### <span data-ttu-id="d3871-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3871-113">-AccountName</span></span>
<span data-ttu-id="d3871-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3871-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3871-115">-Confirm</span></span>
<span data-ttu-id="d3871-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3871-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3871-117">-DefaultProfile</span></span>
<span data-ttu-id="d3871-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3871-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3871-119">-InputObject</span></span>
<span data-ttu-id="d3871-120">Gremlin 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3871-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d3871-121">-Name</span></span>
<span data-ttu-id="d3871-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-122">Database name.</span></span>

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

### <span data-ttu-id="d3871-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3871-123">-ParentObject</span></span>
<span data-ttu-id="d3871-124">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d3871-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d3871-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3871-125">-ResourceGroupName</span></span>
<span data-ttu-id="d3871-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d3871-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="d3871-127">-ThroughputType</span></span>
<span data-ttu-id="d3871-128">마이그레이션할 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="d3871-129">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d3871-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3871-130">-WhatIf</span></span>
<span data-ttu-id="d3871-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d3871-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3871-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3871-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3871-133">CommonParameters</span></span>
<span data-ttu-id="d3871-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3871-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3871-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3871-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3871-136">입력</span><span class="sxs-lookup"><span data-stu-id="d3871-136">INPUTS</span></span>

### <span data-ttu-id="d3871-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="d3871-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="d3871-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d3871-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="d3871-139">출력</span><span class="sxs-lookup"><span data-stu-id="d3871-139">OUTPUTS</span></span>

### <span data-ttu-id="d3871-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d3871-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d3871-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3871-141">NOTES</span></span>

## <span data-ttu-id="d3871-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3871-142">RELATED LINKS</span></span>
