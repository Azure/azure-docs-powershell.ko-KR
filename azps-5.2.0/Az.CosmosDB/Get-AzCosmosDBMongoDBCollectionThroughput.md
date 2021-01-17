---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332673"
---
# <span data-ttu-id="1d371-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="1d371-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="1d371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d371-102">SYNOPSIS</span></span>
<span data-ttu-id="1d371-103">MongoDB 컬렉션의 CosmosDB 데이터당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="1d371-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d371-104">SYNTAX</span></span>

### <span data-ttu-id="1d371-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d371-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d371-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d371-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d371-107">설명</span><span class="sxs-lookup"><span data-stu-id="1d371-107">DESCRIPTION</span></span>
<span data-ttu-id="1d371-108">**Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet은 MongoDB 컬렉션의 프로시저 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="1d371-109">예제</span><span class="sxs-lookup"><span data-stu-id="1d371-109">EXAMPLES</span></span>

### <span data-ttu-id="1d371-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d371-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="1d371-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d371-111">PARAMETERS</span></span>

### <span data-ttu-id="1d371-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d371-112">-AccountName</span></span>
<span data-ttu-id="1d371-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d371-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d371-114">-Confirm</span></span>
<span data-ttu-id="1d371-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d371-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d371-116">-DatabaseName</span></span>
<span data-ttu-id="1d371-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-117">Database name.</span></span>

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

### <span data-ttu-id="1d371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d371-118">-DefaultProfile</span></span>
<span data-ttu-id="1d371-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d371-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d371-120">-InputObject</span></span>
<span data-ttu-id="1d371-121">제공된 경우 cmdlet은 해당 처리률 값이 있는 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d371-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1d371-122">-Name</span></span>
<span data-ttu-id="1d371-123">컬렉션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-123">Collection name.</span></span>

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

### <span data-ttu-id="1d371-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d371-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d371-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1d371-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d371-126">-WhatIf</span></span>
<span data-ttu-id="1d371-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1d371-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d371-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d371-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d371-129">CommonParameters</span></span>
<span data-ttu-id="1d371-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d371-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d371-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d371-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d371-132">입력</span><span class="sxs-lookup"><span data-stu-id="1d371-132">INPUTS</span></span>

### <span data-ttu-id="1d371-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="1d371-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="1d371-134">출력</span><span class="sxs-lookup"><span data-stu-id="1d371-134">OUTPUTS</span></span>

### <span data-ttu-id="1d371-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1d371-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1d371-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d371-136">NOTES</span></span>

## <span data-ttu-id="1d371-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d371-137">RELATED LINKS</span></span>