---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042184"
---
# <span data-ttu-id="bc840-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="bc840-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="bc840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc840-102">SYNOPSIS</span></span>
<span data-ttu-id="bc840-103">CosmosDB MongoDB Collection의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bc840-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc840-104">SYNTAX</span></span>

### <span data-ttu-id="bc840-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc840-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc840-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc840-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc840-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc840-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc840-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bc840-108">EXAMPLES</span></span>

### <span data-ttu-id="bc840-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc840-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="bc840-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="bc840-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="bc840-111">변수</span><span class="sxs-lookup"><span data-stu-id="bc840-111">PARAMETERS</span></span>

### <span data-ttu-id="bc840-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bc840-112">-AccountName</span></span>
<span data-ttu-id="bc840-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bc840-114">-확인</span><span class="sxs-lookup"><span data-stu-id="bc840-114">-Confirm</span></span>
<span data-ttu-id="bc840-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc840-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc840-116">-DatabaseName</span></span>
<span data-ttu-id="bc840-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-117">Database name.</span></span>

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

### <span data-ttu-id="bc840-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc840-118">-DefaultProfile</span></span>
<span data-ttu-id="bc840-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc840-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc840-120">-InputObject</span></span>
<span data-ttu-id="bc840-121">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-121">Mongo Database object.</span></span>

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

### <span data-ttu-id="bc840-122">-이름</span><span class="sxs-lookup"><span data-stu-id="bc840-122">-Name</span></span>
<span data-ttu-id="bc840-123">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-123">Collection name.</span></span>

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

### <span data-ttu-id="bc840-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bc840-124">-ParentObject</span></span>
<span data-ttu-id="bc840-125">Mongo 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="bc840-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc840-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc840-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-127">Name of resource group.</span></span>

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

### <span data-ttu-id="bc840-128">-처리량</span><span class="sxs-lookup"><span data-stu-id="bc840-128">-Throughput</span></span>
<span data-ttu-id="bc840-129">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="bc840-130">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-130">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc840-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc840-131">-WhatIf</span></span>
<span data-ttu-id="bc840-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc840-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc840-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc840-134">CommonParameters</span></span>
<span data-ttu-id="bc840-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc840-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc840-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc840-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc840-137">입력</span><span class="sxs-lookup"><span data-stu-id="bc840-137">INPUTS</span></span>

### <span data-ttu-id="bc840-138">CosmosDB. PSMongoDBDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="bc840-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="bc840-139">출력</span><span class="sxs-lookup"><span data-stu-id="bc840-139">OUTPUTS</span></span>

### <span data-ttu-id="bc840-140">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="bc840-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bc840-141">상속자</span><span class="sxs-lookup"><span data-stu-id="bc840-141">NOTES</span></span>

## <span data-ttu-id="bc840-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc840-142">RELATED LINKS</span></span>
