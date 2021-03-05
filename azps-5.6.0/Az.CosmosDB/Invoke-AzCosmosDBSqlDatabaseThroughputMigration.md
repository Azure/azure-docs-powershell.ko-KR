---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 3a457002fc683c6082a0fad705666a177be93482
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004352"
---
# <span data-ttu-id="ce573-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="ce573-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="ce573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce573-102">SYNOPSIS</span></span>
<span data-ttu-id="ce573-103">이 방법을 사용하여 자동 조정된 작업량은 수동 작업량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="ce573-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce573-104">SYNTAX</span></span>

### <span data-ttu-id="ce573-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce573-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce573-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce573-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce573-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce573-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce573-108">설명</span><span class="sxs-lookup"><span data-stu-id="ce573-108">DESCRIPTION</span></span>
<span data-ttu-id="ce573-109">ThroughpyteType paramter는 마이그레이션할 수 있는 이루어 를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="ce573-110">예제</span><span class="sxs-lookup"><span data-stu-id="ce573-110">EXAMPLES</span></span>

### <span data-ttu-id="ce573-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce573-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```

## <span data-ttu-id="ce573-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce573-112">PARAMETERS</span></span>

### <span data-ttu-id="ce573-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ce573-113">-AccountName</span></span>
<span data-ttu-id="ce573-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ce573-115">-확인</span><span class="sxs-lookup"><span data-stu-id="ce573-115">-Confirm</span></span>
<span data-ttu-id="ce573-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce573-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce573-117">-DefaultProfile</span></span>
<span data-ttu-id="ce573-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce573-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce573-119">-InputObject</span></span>
<span data-ttu-id="ce573-120">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce573-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ce573-121">-Name</span></span>
<span data-ttu-id="ce573-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-122">Database name.</span></span>

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

### <span data-ttu-id="ce573-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ce573-123">-ParentObject</span></span>
<span data-ttu-id="ce573-124">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ce573-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ce573-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce573-125">-ResourceGroupName</span></span>
<span data-ttu-id="ce573-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-126">Name of resource group.</span></span>

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

### <span data-ttu-id="ce573-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="ce573-127">-ThroughputType</span></span>
<span data-ttu-id="ce573-128">마이그레이션할 수 있는 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="ce573-129">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="ce573-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce573-130">-WhatIf</span></span>
<span data-ttu-id="ce573-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce573-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce573-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce573-133">CommonParameters</span></span>
<span data-ttu-id="ce573-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce573-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce573-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce573-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce573-136">입력</span><span class="sxs-lookup"><span data-stu-id="ce573-136">INPUTS</span></span>

### <span data-ttu-id="ce573-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="ce573-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="ce573-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ce573-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="ce573-139">출력</span><span class="sxs-lookup"><span data-stu-id="ce573-139">OUTPUTS</span></span>

### <span data-ttu-id="ce573-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ce573-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ce573-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce573-141">NOTES</span></span>

## <span data-ttu-id="ce573-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce573-142">RELATED LINKS</span></span>
