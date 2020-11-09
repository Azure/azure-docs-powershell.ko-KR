---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307280"
---
# <span data-ttu-id="46291-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="46291-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="46291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46291-102">SYNOPSIS</span></span>
<span data-ttu-id="46291-103">MongoDB 컬렉션의 CosmosDB 처리량 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46291-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="46291-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46291-104">SYNTAX</span></span>

### <span data-ttu-id="46291-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="46291-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46291-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46291-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46291-107">설명은</span><span class="sxs-lookup"><span data-stu-id="46291-107">DESCRIPTION</span></span>
<span data-ttu-id="46291-108">**AzCosmosDBMongoDBCollectionThroughput** Cmdlet은 MongoDB 컬렉션의 처리량 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46291-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="46291-109">예제의</span><span class="sxs-lookup"><span data-stu-id="46291-109">EXAMPLES</span></span>

### <span data-ttu-id="46291-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="46291-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="46291-111">변수</span><span class="sxs-lookup"><span data-stu-id="46291-111">PARAMETERS</span></span>

### <span data-ttu-id="46291-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46291-112">-AccountName</span></span>
<span data-ttu-id="46291-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46291-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46291-114">-확인</span><span class="sxs-lookup"><span data-stu-id="46291-114">-Confirm</span></span>
<span data-ttu-id="46291-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46291-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46291-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="46291-116">-DatabaseName</span></span>
<span data-ttu-id="46291-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46291-117">Database name.</span></span>

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

### <span data-ttu-id="46291-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46291-118">-DefaultProfile</span></span>
<span data-ttu-id="46291-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46291-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46291-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46291-120">-InputObject</span></span>
<span data-ttu-id="46291-121">그런 다음 cmdlet은 해당 처리 값을 사용 하 여 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46291-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="46291-122">-이름</span><span class="sxs-lookup"><span data-stu-id="46291-122">-Name</span></span>
<span data-ttu-id="46291-123">모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46291-123">Collection name.</span></span>

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

### <span data-ttu-id="46291-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46291-124">-ResourceGroupName</span></span>
<span data-ttu-id="46291-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46291-125">Name of resource group.</span></span>

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

### <span data-ttu-id="46291-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46291-126">-WhatIf</span></span>
<span data-ttu-id="46291-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46291-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46291-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46291-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46291-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46291-129">CommonParameters</span></span>
<span data-ttu-id="46291-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46291-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46291-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46291-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46291-132">입력</span><span class="sxs-lookup"><span data-stu-id="46291-132">INPUTS</span></span>

### <span data-ttu-id="46291-133">CosmosDB. PSMongoDBCollectionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="46291-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="46291-134">출력</span><span class="sxs-lookup"><span data-stu-id="46291-134">OUTPUTS</span></span>

### <span data-ttu-id="46291-135">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="46291-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="46291-136">상속자</span><span class="sxs-lookup"><span data-stu-id="46291-136">NOTES</span></span>

## <span data-ttu-id="46291-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46291-137">RELATED LINKS</span></span>
