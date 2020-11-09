---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306782"
---
# <span data-ttu-id="0c81d-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="0c81d-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="0c81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c81d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c81d-103">CosmosDB MongoDB 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="0c81d-104">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="0c81d-105">구문과</span><span class="sxs-lookup"><span data-stu-id="0c81d-105">SYNTAX</span></span>

### <span data-ttu-id="0c81d-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c81d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c81d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c81d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c81d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c81d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c81d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0c81d-109">DESCRIPTION</span></span>
<span data-ttu-id="0c81d-110">CosmosDB MongoDB 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="0c81d-111">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="0c81d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0c81d-112">EXAMPLES</span></span>

### <span data-ttu-id="0c81d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c81d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="0c81d-114">변수</span><span class="sxs-lookup"><span data-stu-id="0c81d-114">PARAMETERS</span></span>

### <span data-ttu-id="0c81d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c81d-115">-AccountName</span></span>
<span data-ttu-id="0c81d-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0c81d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0c81d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0c81d-118">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0c81d-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0c81d-119">-Confirm</span></span>
<span data-ttu-id="0c81d-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c81d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c81d-121">-DefaultProfile</span></span>
<span data-ttu-id="0c81d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c81d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c81d-123">-InputObject</span></span>
<span data-ttu-id="0c81d-124">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c81d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="0c81d-125">-Name</span></span>
<span data-ttu-id="0c81d-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-126">Database name.</span></span>

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

### <span data-ttu-id="0c81d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0c81d-127">-ParentObject</span></span>
<span data-ttu-id="0c81d-128">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="0c81d-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0c81d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c81d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c81d-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="0c81d-131">-처리량</span><span class="sxs-lookup"><span data-stu-id="0c81d-131">-Throughput</span></span>
<span data-ttu-id="0c81d-132">Mongo 데이터베이스의 처리량 (는 o/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="0c81d-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="0c81d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c81d-134">-WhatIf</span></span>
<span data-ttu-id="0c81d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c81d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c81d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c81d-137">CommonParameters</span></span>
<span data-ttu-id="0c81d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c81d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c81d-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c81d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c81d-140">입력</span><span class="sxs-lookup"><span data-stu-id="0c81d-140">INPUTS</span></span>

### <span data-ttu-id="0c81d-141">않아야</span><span class="sxs-lookup"><span data-stu-id="0c81d-141">None</span></span>

## <span data-ttu-id="0c81d-142">출력</span><span class="sxs-lookup"><span data-stu-id="0c81d-142">OUTPUTS</span></span>

### <span data-ttu-id="0c81d-143">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="0c81d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="0c81d-144">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="0c81d-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="0c81d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0c81d-145">NOTES</span></span>

## <span data-ttu-id="0c81d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c81d-146">RELATED LINKS</span></span>
