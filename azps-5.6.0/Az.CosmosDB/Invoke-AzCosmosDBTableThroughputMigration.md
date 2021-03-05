---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 2511ddc7174d4b76ec6d5df5bcbcd334f423a882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996851"
---
# <span data-ttu-id="a10f1-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="a10f1-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="a10f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a10f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a10f1-103">이 방법을 사용하여 자동 조정된 작업량은 수동 작업량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="a10f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="a10f1-104">SYNTAX</span></span>

### <span data-ttu-id="a10f1-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a10f1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a10f1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a10f1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a10f1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a10f1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a10f1-108">설명</span><span class="sxs-lookup"><span data-stu-id="a10f1-108">DESCRIPTION</span></span>
<span data-ttu-id="a10f1-109">ThroughpyteType paramter는 마이그레이션할 수 있는 이루어 를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="a10f1-110">예제</span><span class="sxs-lookup"><span data-stu-id="a10f1-110">EXAMPLES</span></span>

### <span data-ttu-id="a10f1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a10f1-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="a10f1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a10f1-112">PARAMETERS</span></span>

### <span data-ttu-id="a10f1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a10f1-113">-AccountName</span></span>
<span data-ttu-id="a10f1-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a10f1-115">-확인</span><span class="sxs-lookup"><span data-stu-id="a10f1-115">-Confirm</span></span>
<span data-ttu-id="a10f1-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a10f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10f1-117">-DefaultProfile</span></span>
<span data-ttu-id="a10f1-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a10f1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a10f1-119">-InputObject</span></span>
<span data-ttu-id="a10f1-120">테이블 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a10f1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a10f1-121">-Name</span></span>
<span data-ttu-id="a10f1-122">표의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-122">Name of the Table.</span></span>

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

### <span data-ttu-id="a10f1-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a10f1-123">-ParentObject</span></span>
<span data-ttu-id="a10f1-124">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="a10f1-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a10f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a10f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="a10f1-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a10f1-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="a10f1-127">-ThroughputType</span></span>
<span data-ttu-id="a10f1-128">마이그레이션할 수 있는 데이터 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="a10f1-129">가능한 값은 자동 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="a10f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a10f1-130">-WhatIf</span></span>
<span data-ttu-id="a10f1-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a10f1-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a10f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10f1-133">CommonParameters</span></span>
<span data-ttu-id="a10f1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a10f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10f1-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a10f1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10f1-136">입력</span><span class="sxs-lookup"><span data-stu-id="a10f1-136">INPUTS</span></span>

### <span data-ttu-id="a10f1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="a10f1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="a10f1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a10f1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="a10f1-139">출력</span><span class="sxs-lookup"><span data-stu-id="a10f1-139">OUTPUTS</span></span>

### <span data-ttu-id="a10f1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a10f1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a10f1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a10f1-141">NOTES</span></span>

## <span data-ttu-id="a10f1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a10f1-142">RELATED LINKS</span></span>
