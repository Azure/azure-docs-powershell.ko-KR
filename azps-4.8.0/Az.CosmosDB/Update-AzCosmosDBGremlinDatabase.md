---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212554"
---
# <span data-ttu-id="befb4-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="befb4-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="befb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befb4-102">SYNOPSIS</span></span>
<span data-ttu-id="befb4-103">CosmosDB Gremlin 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="befb4-104">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="befb4-105">구문과</span><span class="sxs-lookup"><span data-stu-id="befb4-105">SYNTAX</span></span>

### <span data-ttu-id="befb4-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="befb4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="befb4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="befb4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="befb4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="befb4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="befb4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="befb4-109">DESCRIPTION</span></span>
<span data-ttu-id="befb4-110">CosmosDB Gremlin 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="befb4-111">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="befb4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="befb4-112">EXAMPLES</span></span>

### <span data-ttu-id="befb4-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="befb4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="befb4-114">변수</span><span class="sxs-lookup"><span data-stu-id="befb4-114">PARAMETERS</span></span>

### <span data-ttu-id="befb4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="befb4-115">-AccountName</span></span>
<span data-ttu-id="befb4-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="befb4-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="befb4-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="befb4-118">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="befb4-119">-확인</span><span class="sxs-lookup"><span data-stu-id="befb4-119">-Confirm</span></span>
<span data-ttu-id="befb4-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="befb4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befb4-121">-DefaultProfile</span></span>
<span data-ttu-id="befb4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="befb4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="befb4-123">-InputObject</span></span>
<span data-ttu-id="befb4-124">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="befb4-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="befb4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="befb4-125">-Name</span></span>
<span data-ttu-id="befb4-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-126">Database name.</span></span>

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

### <span data-ttu-id="befb4-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="befb4-127">-ParentObject</span></span>
<span data-ttu-id="befb4-128">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="befb4-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="befb4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befb4-129">-ResourceGroupName</span></span>
<span data-ttu-id="befb4-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-130">Name of resource group.</span></span>

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

### <span data-ttu-id="befb4-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="befb4-131">-Throughput</span></span>
<span data-ttu-id="befb4-132">Gremlin 데이터베이스의 처리량 (. e 1/s)</span><span class="sxs-lookup"><span data-stu-id="befb4-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="befb4-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-133">Default value is 400.</span></span>

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

### <span data-ttu-id="befb4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="befb4-134">-WhatIf</span></span>
<span data-ttu-id="befb4-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="befb4-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="befb4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befb4-137">CommonParameters</span></span>
<span data-ttu-id="befb4-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="befb4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befb4-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="befb4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befb4-140">입력</span><span class="sxs-lookup"><span data-stu-id="befb4-140">INPUTS</span></span>

### <span data-ttu-id="befb4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="befb4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="befb4-142">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="befb4-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="befb4-143">출력</span><span class="sxs-lookup"><span data-stu-id="befb4-143">OUTPUTS</span></span>

### <span data-ttu-id="befb4-144">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="befb4-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="befb4-145">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="befb4-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="befb4-146">상속자</span><span class="sxs-lookup"><span data-stu-id="befb4-146">NOTES</span></span>

## <span data-ttu-id="befb4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="befb4-147">RELATED LINKS</span></span>
