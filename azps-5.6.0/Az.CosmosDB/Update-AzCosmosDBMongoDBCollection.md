---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 2458c31ba75470c5d2b5bb2b73d817eb58c5bc61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977307"
---
# <span data-ttu-id="f98a8-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="f98a8-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="f98a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f98a8-103">CosmosDB MongoDB 컬렉션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="f98a8-104">기존 컬렉션을 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="f98a8-105">구문</span><span class="sxs-lookup"><span data-stu-id="f98a8-105">SYNTAX</span></span>

### <span data-ttu-id="f98a8-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f98a8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98a8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98a8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f98a8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98a8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f98a8-109">설명</span><span class="sxs-lookup"><span data-stu-id="f98a8-109">DESCRIPTION</span></span>
<span data-ttu-id="f98a8-110">CosmosDB MongoDB 컬렉션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="f98a8-111">기존 컬렉션을 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="f98a8-112">예제</span><span class="sxs-lookup"><span data-stu-id="f98a8-112">EXAMPLES</span></span>

### <span data-ttu-id="f98a8-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f98a8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="f98a8-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f98a8-114">PARAMETERS</span></span>

### <span data-ttu-id="f98a8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f98a8-115">-AccountName</span></span>
<span data-ttu-id="f98a8-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f98a8-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="f98a8-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="f98a8-118">분석 저장소용 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="f98a8-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f98a8-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f98a8-120">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f98a8-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f98a8-121">-Confirm</span></span>
<span data-ttu-id="f98a8-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98a8-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f98a8-123">-DatabaseName</span></span>
<span data-ttu-id="f98a8-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-124">Database name.</span></span>

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

### <span data-ttu-id="f98a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98a8-125">-DefaultProfile</span></span>
<span data-ttu-id="f98a8-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98a8-127">-Index</span><span class="sxs-lookup"><span data-stu-id="f98a8-127">-Index</span></span>
<span data-ttu-id="f98a8-128">PSMongoIndex 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98a8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f98a8-129">-InputObject</span></span>
<span data-ttu-id="f98a8-130">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98a8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f98a8-131">-Name</span></span>
<span data-ttu-id="f98a8-132">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-132">Collection name.</span></span>

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

### <span data-ttu-id="f98a8-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f98a8-133">-ParentObject</span></span>
<span data-ttu-id="f98a8-134">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98a8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98a8-135">-ResourceGroupName</span></span>
<span data-ttu-id="f98a8-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-136">Name of resource group.</span></span>

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

### <span data-ttu-id="f98a8-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="f98a8-137">-Shard</span></span>
<span data-ttu-id="f98a8-138">키 경로의 셰이드링</span><span class="sxs-lookup"><span data-stu-id="f98a8-138">Sharding key path.</span></span>

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

### <span data-ttu-id="f98a8-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f98a8-139">-Throughput</span></span>
<span data-ttu-id="f98a8-140">RU/s SQL 컨테이너의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="f98a8-141">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-141">Default value is 400.</span></span>

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

### <span data-ttu-id="f98a8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98a8-142">-WhatIf</span></span>
<span data-ttu-id="f98a8-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98a8-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98a8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98a8-145">CommonParameters</span></span>
<span data-ttu-id="f98a8-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f98a8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98a8-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f98a8-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98a8-148">입력</span><span class="sxs-lookup"><span data-stu-id="f98a8-148">INPUTS</span></span>

### <span data-ttu-id="f98a8-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f98a8-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="f98a8-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f98a8-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="f98a8-151">출력</span><span class="sxs-lookup"><span data-stu-id="f98a8-151">OUTPUTS</span></span>

### <span data-ttu-id="f98a8-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="f98a8-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="f98a8-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f98a8-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f98a8-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f98a8-154">NOTES</span></span>

## <span data-ttu-id="f98a8-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f98a8-155">RELATED LINKS</span></span>
