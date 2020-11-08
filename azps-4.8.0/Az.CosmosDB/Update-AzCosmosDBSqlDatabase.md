---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212852"
---
# <span data-ttu-id="8e763-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e763-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="8e763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e763-102">SYNOPSIS</span></span>
<span data-ttu-id="8e763-103">CosmosDB Sql 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="8e763-104">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="8e763-105">구문과</span><span class="sxs-lookup"><span data-stu-id="8e763-105">SYNTAX</span></span>

### <span data-ttu-id="8e763-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e763-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e763-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e763-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e763-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e763-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e763-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8e763-109">DESCRIPTION</span></span>
<span data-ttu-id="8e763-110">CosmosDB Sql 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="8e763-111">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="8e763-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8e763-112">EXAMPLES</span></span>

### <span data-ttu-id="8e763-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e763-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="8e763-114">변수</span><span class="sxs-lookup"><span data-stu-id="8e763-114">PARAMETERS</span></span>

### <span data-ttu-id="8e763-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e763-115">-AccountName</span></span>
<span data-ttu-id="8e763-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8e763-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8e763-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8e763-118">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8e763-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8e763-119">-Confirm</span></span>
<span data-ttu-id="8e763-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e763-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e763-121">-DefaultProfile</span></span>
<span data-ttu-id="8e763-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e763-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e763-123">-InputObject</span></span>
<span data-ttu-id="8e763-124">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="8e763-124">Sql Database object.</span></span>

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

### <span data-ttu-id="8e763-125">-이름</span><span class="sxs-lookup"><span data-stu-id="8e763-125">-Name</span></span>
<span data-ttu-id="8e763-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-126">Database name.</span></span>

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

### <span data-ttu-id="8e763-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e763-127">-ParentObject</span></span>
<span data-ttu-id="8e763-128">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="8e763-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8e763-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e763-129">-ResourceGroupName</span></span>
<span data-ttu-id="8e763-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-130">Name of resource group.</span></span>

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

### <span data-ttu-id="8e763-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="8e763-131">-Throughput</span></span>
<span data-ttu-id="8e763-132">SQL 데이터베이스의 처리량 (#/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="8e763-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-133">Default value is 400.</span></span>

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

### <span data-ttu-id="8e763-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e763-134">-WhatIf</span></span>
<span data-ttu-id="8e763-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e763-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e763-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e763-137">CommonParameters</span></span>
<span data-ttu-id="8e763-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e763-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e763-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e763-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e763-140">입력</span><span class="sxs-lookup"><span data-stu-id="8e763-140">INPUTS</span></span>

### <span data-ttu-id="8e763-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8e763-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="8e763-142">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="8e763-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="8e763-143">출력</span><span class="sxs-lookup"><span data-stu-id="8e763-143">OUTPUTS</span></span>

### <span data-ttu-id="8e763-144">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="8e763-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="8e763-145">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="8e763-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="8e763-146">상속자</span><span class="sxs-lookup"><span data-stu-id="8e763-146">NOTES</span></span>

## <span data-ttu-id="8e763-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e763-147">RELATED LINKS</span></span>
