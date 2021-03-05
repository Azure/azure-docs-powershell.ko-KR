---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 66ca19099d4562da3add57411a16be1a0573ea02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977296"
---
# <span data-ttu-id="279db-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="279db-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="279db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="279db-102">SYNOPSIS</span></span>
<span data-ttu-id="279db-103">CosmosDB MongoDB 컬렉션의 사용 데이터 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="279db-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="279db-104">구문</span><span class="sxs-lookup"><span data-stu-id="279db-104">SYNTAX</span></span>

### <span data-ttu-id="279db-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="279db-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279db-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279db-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279db-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279db-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279db-108">설명</span><span class="sxs-lookup"><span data-stu-id="279db-108">DESCRIPTION</span></span>
<span data-ttu-id="279db-109">CosmosDB MongoDB 컬렉션의 사용 데이터 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="279db-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="279db-110">예제</span><span class="sxs-lookup"><span data-stu-id="279db-110">EXAMPLES</span></span>

### <span data-ttu-id="279db-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="279db-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="279db-112">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="279db-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="279db-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="279db-113">PARAMETERS</span></span>

### <span data-ttu-id="279db-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="279db-114">-AccountName</span></span>
<span data-ttu-id="279db-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="279db-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="279db-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="279db-117">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="279db-118">-확인</span><span class="sxs-lookup"><span data-stu-id="279db-118">-Confirm</span></span>
<span data-ttu-id="279db-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="279db-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279db-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="279db-120">-DatabaseName</span></span>
<span data-ttu-id="279db-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-121">Database name.</span></span>

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

### <span data-ttu-id="279db-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279db-122">-DefaultProfile</span></span>
<span data-ttu-id="279db-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279db-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279db-124">-InputObject</span></span>
<span data-ttu-id="279db-125">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="279db-126">-Name</span><span class="sxs-lookup"><span data-stu-id="279db-126">-Name</span></span>
<span data-ttu-id="279db-127">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-127">Collection name.</span></span>

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

### <span data-ttu-id="279db-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="279db-128">-ParentObject</span></span>
<span data-ttu-id="279db-129">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="279db-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279db-130">-ResourceGroupName</span></span>
<span data-ttu-id="279db-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-131">Name of resource group.</span></span>

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

### <span data-ttu-id="279db-132">-Throughput</span><span class="sxs-lookup"><span data-stu-id="279db-132">-Throughput</span></span>
<span data-ttu-id="279db-133">RU/s SQL 컨테이너의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="279db-134">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="279db-134">Default value is 400.</span></span>

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

### <span data-ttu-id="279db-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279db-135">-WhatIf</span></span>
<span data-ttu-id="279db-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="279db-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279db-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="279db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279db-138">CommonParameters</span></span>
<span data-ttu-id="279db-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="279db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279db-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="279db-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279db-141">입력</span><span class="sxs-lookup"><span data-stu-id="279db-141">INPUTS</span></span>

### <span data-ttu-id="279db-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="279db-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="279db-143">출력</span><span class="sxs-lookup"><span data-stu-id="279db-143">OUTPUTS</span></span>

### <span data-ttu-id="279db-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="279db-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="279db-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="279db-145">NOTES</span></span>

## <span data-ttu-id="279db-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="279db-146">RELATED LINKS</span></span>
