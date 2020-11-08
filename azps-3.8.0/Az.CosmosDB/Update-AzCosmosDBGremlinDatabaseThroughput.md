---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 75ea7849424d8587f4eb4151bde63f31ea35676f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879858"
---
# <span data-ttu-id="4d49c-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="4d49c-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="4d49c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d49c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d49c-103">CosmosDB Gremlin 데이터베이스의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="4d49c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d49c-104">SYNTAX</span></span>

### <span data-ttu-id="4d49c-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d49c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d49c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d49c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d49c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d49c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d49c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4d49c-108">EXAMPLES</span></span>

### <span data-ttu-id="4d49c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d49c-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="4d49c-110">변수</span><span class="sxs-lookup"><span data-stu-id="4d49c-110">PARAMETERS</span></span>

### <span data-ttu-id="4d49c-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d49c-111">-AccountName</span></span>
<span data-ttu-id="4d49c-112">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d49c-113">-확인</span><span class="sxs-lookup"><span data-stu-id="4d49c-113">-Confirm</span></span>
<span data-ttu-id="4d49c-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d49c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d49c-115">-DefaultProfile</span></span>
<span data-ttu-id="4d49c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d49c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d49c-117">-InputObject</span></span>
<span data-ttu-id="4d49c-118">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="4d49c-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4d49c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4d49c-119">-Name</span></span>
<span data-ttu-id="4d49c-120">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-120">Database name.</span></span>

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

### <span data-ttu-id="4d49c-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d49c-121">-ParentObject</span></span>
<span data-ttu-id="4d49c-122">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="4d49c-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d49c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d49c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d49c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-124">Name of resource group.</span></span>

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

### <span data-ttu-id="4d49c-125">-처리량</span><span class="sxs-lookup"><span data-stu-id="4d49c-125">-Throughput</span></span>
<span data-ttu-id="4d49c-126">Gremlin 데이터베이스의 처리량 (. e 1/s)</span><span class="sxs-lookup"><span data-stu-id="4d49c-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="4d49c-127">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-127">Default value is 400.</span></span>

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

### <span data-ttu-id="4d49c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d49c-128">-WhatIf</span></span>
<span data-ttu-id="4d49c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d49c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d49c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d49c-131">CommonParameters</span></span>
<span data-ttu-id="4d49c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d49c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d49c-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d49c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d49c-134">입력</span><span class="sxs-lookup"><span data-stu-id="4d49c-134">INPUTS</span></span>

### <span data-ttu-id="4d49c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4d49c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4d49c-136">출력</span><span class="sxs-lookup"><span data-stu-id="4d49c-136">OUTPUTS</span></span>

### <span data-ttu-id="4d49c-137">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="4d49c-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4d49c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="4d49c-138">NOTES</span></span>

## <span data-ttu-id="4d49c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d49c-139">RELATED LINKS</span></span>