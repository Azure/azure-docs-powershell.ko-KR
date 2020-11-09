---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307181"
---
# <span data-ttu-id="495a2-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="495a2-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="495a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495a2-102">SYNOPSIS</span></span>
<span data-ttu-id="495a2-103">이를 사용 하 여 자동 크기 조정 처리량을 수동 처리량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="495a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="495a2-104">SYNTAX</span></span>

### <span data-ttu-id="495a2-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="495a2-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="495a2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="495a2-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495a2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="495a2-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="495a2-108">DESCRIPTION</span></span>
<span data-ttu-id="495a2-109">ThroughpyteType 매개 변수는 마이그레이션할 처리량을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="495a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="495a2-110">EXAMPLES</span></span>

### <span data-ttu-id="495a2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="495a2-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="495a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="495a2-112">PARAMETERS</span></span>

### <span data-ttu-id="495a2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="495a2-113">-AccountName</span></span>
<span data-ttu-id="495a2-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="495a2-115">-확인</span><span class="sxs-lookup"><span data-stu-id="495a2-115">-Confirm</span></span>
<span data-ttu-id="495a2-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495a2-117">-DefaultProfile</span></span>
<span data-ttu-id="495a2-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="495a2-119">-InputObject</span></span>
<span data-ttu-id="495a2-120">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="495a2-121">-이름</span><span class="sxs-lookup"><span data-stu-id="495a2-121">-Name</span></span>
<span data-ttu-id="495a2-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-122">Database name.</span></span>

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

### <span data-ttu-id="495a2-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="495a2-123">-ParentObject</span></span>
<span data-ttu-id="495a2-124">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="495a2-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="495a2-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-126">Name of resource group.</span></span>

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

### <span data-ttu-id="495a2-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="495a2-127">-ThroughputType</span></span>
<span data-ttu-id="495a2-128">마이그레이션할 처리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="495a2-129">사용할 수 있는 값은 자동 크기 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="495a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495a2-130">-WhatIf</span></span>
<span data-ttu-id="495a2-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495a2-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495a2-133">CommonParameters</span></span>
<span data-ttu-id="495a2-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="495a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495a2-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="495a2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495a2-136">입력</span><span class="sxs-lookup"><span data-stu-id="495a2-136">INPUTS</span></span>

### <span data-ttu-id="495a2-137">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="495a2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="495a2-138">출력</span><span class="sxs-lookup"><span data-stu-id="495a2-138">OUTPUTS</span></span>

### <span data-ttu-id="495a2-139">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="495a2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="495a2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="495a2-140">NOTES</span></span>

## <span data-ttu-id="495a2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="495a2-141">RELATED LINKS</span></span>
