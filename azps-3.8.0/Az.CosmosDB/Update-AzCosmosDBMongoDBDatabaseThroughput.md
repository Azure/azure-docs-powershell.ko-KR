---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d90df542fd2acc925531f4bf9da7244ea1831a63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042182"
---
# <span data-ttu-id="73063-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="73063-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="73063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73063-102">SYNOPSIS</span></span>
<span data-ttu-id="73063-103">CosmosDB MongoDB 데이터베이스의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73063-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="73063-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73063-104">SYNTAX</span></span>

### <span data-ttu-id="73063-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="73063-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73063-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73063-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73063-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73063-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73063-108">예제의</span><span class="sxs-lookup"><span data-stu-id="73063-108">EXAMPLES</span></span>

### <span data-ttu-id="73063-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="73063-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="73063-110">변수</span><span class="sxs-lookup"><span data-stu-id="73063-110">PARAMETERS</span></span>

### <span data-ttu-id="73063-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73063-111">-AccountName</span></span>
<span data-ttu-id="73063-112">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73063-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="73063-113">-확인</span><span class="sxs-lookup"><span data-stu-id="73063-113">-Confirm</span></span>
<span data-ttu-id="73063-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73063-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73063-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73063-115">-DefaultProfile</span></span>
<span data-ttu-id="73063-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73063-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73063-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73063-117">-InputObject</span></span>
<span data-ttu-id="73063-118">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="73063-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="73063-119">-이름</span><span class="sxs-lookup"><span data-stu-id="73063-119">-Name</span></span>
<span data-ttu-id="73063-120">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73063-120">Database name.</span></span>

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

### <span data-ttu-id="73063-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="73063-121">-ParentObject</span></span>
<span data-ttu-id="73063-122">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="73063-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73063-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73063-123">-ResourceGroupName</span></span>
<span data-ttu-id="73063-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73063-124">Name of resource group.</span></span>

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

### <span data-ttu-id="73063-125">-처리량</span><span class="sxs-lookup"><span data-stu-id="73063-125">-Throughput</span></span>
<span data-ttu-id="73063-126">Mongo 데이터베이스의 처리량 (는 o/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="73063-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="73063-127">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="73063-127">Default value is 400.</span></span>

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

### <span data-ttu-id="73063-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73063-128">-WhatIf</span></span>
<span data-ttu-id="73063-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73063-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73063-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73063-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73063-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73063-131">CommonParameters</span></span>
<span data-ttu-id="73063-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73063-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73063-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="73063-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73063-134">입력</span><span class="sxs-lookup"><span data-stu-id="73063-134">INPUTS</span></span>

### <span data-ttu-id="73063-135">않아야</span><span class="sxs-lookup"><span data-stu-id="73063-135">None</span></span>

## <span data-ttu-id="73063-136">출력</span><span class="sxs-lookup"><span data-stu-id="73063-136">OUTPUTS</span></span>

### <span data-ttu-id="73063-137">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="73063-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="73063-138">상속자</span><span class="sxs-lookup"><span data-stu-id="73063-138">NOTES</span></span>

## <span data-ttu-id="73063-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73063-139">RELATED LINKS</span></span>
