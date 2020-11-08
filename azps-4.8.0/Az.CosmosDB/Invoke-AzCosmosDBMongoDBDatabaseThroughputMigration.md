---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214632"
---
# <span data-ttu-id="04ce5-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="04ce5-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="04ce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="04ce5-103">이를 사용 하 여 자동 크기 조정 처리량을 수동 처리량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="04ce5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04ce5-104">SYNTAX</span></span>

### <span data-ttu-id="04ce5-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="04ce5-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04ce5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ce5-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ce5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04ce5-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ce5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="04ce5-108">DESCRIPTION</span></span>
<span data-ttu-id="04ce5-109">ThroughpyteType 매개 변수는 마이그레이션할 처리량을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="04ce5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="04ce5-110">EXAMPLES</span></span>

### <span data-ttu-id="04ce5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="04ce5-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="04ce5-112">변수</span><span class="sxs-lookup"><span data-stu-id="04ce5-112">PARAMETERS</span></span>

### <span data-ttu-id="04ce5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04ce5-113">-AccountName</span></span>
<span data-ttu-id="04ce5-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="04ce5-115">-확인</span><span class="sxs-lookup"><span data-stu-id="04ce5-115">-Confirm</span></span>
<span data-ttu-id="04ce5-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ce5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ce5-117">-DefaultProfile</span></span>
<span data-ttu-id="04ce5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ce5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ce5-119">-InputObject</span></span>
<span data-ttu-id="04ce5-120">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="04ce5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="04ce5-121">-Name</span></span>
<span data-ttu-id="04ce5-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-122">Database name.</span></span>

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

### <span data-ttu-id="04ce5-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="04ce5-123">-ParentObject</span></span>
<span data-ttu-id="04ce5-124">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="04ce5-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="04ce5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ce5-125">-ResourceGroupName</span></span>
<span data-ttu-id="04ce5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-126">Name of resource group.</span></span>

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

### <span data-ttu-id="04ce5-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="04ce5-127">-ThroughputType</span></span>
<span data-ttu-id="04ce5-128">마이그레이션할 처리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="04ce5-129">사용할 수 있는 값은 자동 크기 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="04ce5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ce5-130">-WhatIf</span></span>
<span data-ttu-id="04ce5-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ce5-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ce5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ce5-133">CommonParameters</span></span>
<span data-ttu-id="04ce5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ce5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ce5-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="04ce5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ce5-136">입력</span><span class="sxs-lookup"><span data-stu-id="04ce5-136">INPUTS</span></span>

### <span data-ttu-id="04ce5-137">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="04ce5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="04ce5-138">출력</span><span class="sxs-lookup"><span data-stu-id="04ce5-138">OUTPUTS</span></span>

### <span data-ttu-id="04ce5-139">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="04ce5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="04ce5-140">상속자</span><span class="sxs-lookup"><span data-stu-id="04ce5-140">NOTES</span></span>

## <span data-ttu-id="04ce5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04ce5-141">RELATED LINKS</span></span>
