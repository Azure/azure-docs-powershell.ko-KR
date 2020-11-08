---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048371"
---
# <span data-ttu-id="c1c10-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1c10-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="c1c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c10-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c10-103">새 CosmosDB Sql 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="c1c10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1c10-104">SYNTAX</span></span>

### <span data-ttu-id="c1c10-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c1c10-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c10-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c10-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c10-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c1c10-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c10-108">새 CosmosDB Sql 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="c1c10-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c1c10-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c10-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1c10-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="c1c10-111">변수</span><span class="sxs-lookup"><span data-stu-id="c1c10-111">PARAMETERS</span></span>

### <span data-ttu-id="c1c10-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c1c10-112">-AccountName</span></span>
<span data-ttu-id="c1c10-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c1c10-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c1c10-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c1c10-115">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c10-116">-확인</span><span class="sxs-lookup"><span data-stu-id="c1c10-116">-Confirm</span></span>
<span data-ttu-id="c1c10-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c10-118">-DefaultProfile</span></span>
<span data-ttu-id="c1c10-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c10-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c1c10-120">-Name</span></span>
<span data-ttu-id="c1c10-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-121">Database name.</span></span>

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

### <span data-ttu-id="c1c10-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1c10-122">-ParentObject</span></span>
<span data-ttu-id="c1c10-123">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="c1c10-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c1c10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c10-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1c10-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-125">Name of resource group.</span></span>

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

### <span data-ttu-id="c1c10-126">-처리량</span><span class="sxs-lookup"><span data-stu-id="c1c10-126">-Throughput</span></span>
<span data-ttu-id="c1c10-127">SQL 데이터베이스의 처리량 (#/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="c1c10-128">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c10-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c10-129">-WhatIf</span></span>
<span data-ttu-id="c1c10-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c10-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c10-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c10-132">CommonParameters</span></span>
<span data-ttu-id="c1c10-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1c10-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c10-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1c10-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c10-135">입력</span><span class="sxs-lookup"><span data-stu-id="c1c10-135">INPUTS</span></span>

### <span data-ttu-id="c1c10-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c1c10-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c1c10-137">출력</span><span class="sxs-lookup"><span data-stu-id="c1c10-137">OUTPUTS</span></span>

### <span data-ttu-id="c1c10-138">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c1c10-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="c1c10-139">CosmosDB (ConflictingResourceException).</span><span class="sxs-lookup"><span data-stu-id="c1c10-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="c1c10-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c1c10-140">NOTES</span></span>

## <span data-ttu-id="c1c10-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1c10-141">RELATED LINKS</span></span>
