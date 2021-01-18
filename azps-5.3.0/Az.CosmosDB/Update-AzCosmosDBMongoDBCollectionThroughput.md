---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493651"
---
# <span data-ttu-id="26a16-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="26a16-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="26a16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26a16-102">SYNOPSIS</span></span>
<span data-ttu-id="26a16-103">CosmosDB MongoDB 컬렉션의 데이터당 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="26a16-104">구문</span><span class="sxs-lookup"><span data-stu-id="26a16-104">SYNTAX</span></span>

### <span data-ttu-id="26a16-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="26a16-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a16-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a16-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a16-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a16-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a16-108">설명</span><span class="sxs-lookup"><span data-stu-id="26a16-108">DESCRIPTION</span></span>
<span data-ttu-id="26a16-109">CosmosDB MongoDB 컬렉션의 데이터당 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="26a16-110">예제</span><span class="sxs-lookup"><span data-stu-id="26a16-110">EXAMPLES</span></span>

### <span data-ttu-id="26a16-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="26a16-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="26a16-112">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="26a16-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="26a16-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26a16-113">PARAMETERS</span></span>

### <span data-ttu-id="26a16-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26a16-114">-AccountName</span></span>
<span data-ttu-id="26a16-115">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26a16-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="26a16-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="26a16-117">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="26a16-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26a16-118">-Confirm</span></span>
<span data-ttu-id="26a16-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a16-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26a16-120">-DatabaseName</span></span>
<span data-ttu-id="26a16-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-121">Database name.</span></span>

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

### <span data-ttu-id="26a16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a16-122">-DefaultProfile</span></span>
<span data-ttu-id="26a16-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26a16-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26a16-124">-InputObject</span></span>
<span data-ttu-id="26a16-125">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="26a16-126">-Name</span><span class="sxs-lookup"><span data-stu-id="26a16-126">-Name</span></span>
<span data-ttu-id="26a16-127">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-127">Collection name.</span></span>

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

### <span data-ttu-id="26a16-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="26a16-128">-ParentObject</span></span>
<span data-ttu-id="26a16-129">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="26a16-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26a16-130">-ResourceGroupName</span></span>
<span data-ttu-id="26a16-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-131">Name of resource group.</span></span>

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

### <span data-ttu-id="26a16-132">-Throughput</span><span class="sxs-lookup"><span data-stu-id="26a16-132">-Throughput</span></span>
<span data-ttu-id="26a16-133">컨테이너의 SQL(RU/s)</span><span class="sxs-lookup"><span data-stu-id="26a16-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="26a16-134">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-134">Default value is 400.</span></span>

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

### <span data-ttu-id="26a16-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a16-135">-WhatIf</span></span>
<span data-ttu-id="26a16-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="26a16-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a16-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a16-138">CommonParameters</span></span>
<span data-ttu-id="26a16-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26a16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a16-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26a16-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a16-141">입력</span><span class="sxs-lookup"><span data-stu-id="26a16-141">INPUTS</span></span>

### <span data-ttu-id="26a16-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="26a16-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="26a16-143">출력</span><span class="sxs-lookup"><span data-stu-id="26a16-143">OUTPUTS</span></span>

### <span data-ttu-id="26a16-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="26a16-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="26a16-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26a16-145">NOTES</span></span>

## <span data-ttu-id="26a16-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26a16-146">RELATED LINKS</span></span>
