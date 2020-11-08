---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212569"
---
# <span data-ttu-id="3b9ba-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="3b9ba-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="3b9ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9ba-103">Cassandra 테이블의 처리량 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="3b9ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b9ba-104">SYNTAX</span></span>

### <span data-ttu-id="3b9ba-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3b9ba-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9ba-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b9ba-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3b9ba-107">DESCRIPTION</span></span>
<span data-ttu-id="3b9ba-108">**AzCosmosDBCassandraTableThroughput** cmdlet은 지정 된 Keyspace에 해당 하는 처리 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="3b9ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3b9ba-109">EXAMPLES</span></span>

### <span data-ttu-id="3b9ba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3b9ba-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="3b9ba-111">변수</span><span class="sxs-lookup"><span data-stu-id="3b9ba-111">PARAMETERS</span></span>

### <span data-ttu-id="3b9ba-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b9ba-112">-AccountName</span></span>
<span data-ttu-id="3b9ba-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3b9ba-114">-확인</span><span class="sxs-lookup"><span data-stu-id="3b9ba-114">-Confirm</span></span>
<span data-ttu-id="3b9ba-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b9ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9ba-116">-DefaultProfile</span></span>
<span data-ttu-id="3b9ba-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b9ba-118">-InputObject</span></span>
<span data-ttu-id="3b9ba-119">Cassandra Table 개체</span><span class="sxs-lookup"><span data-stu-id="3b9ba-119">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9ba-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="3b9ba-120">-KeyspaceName</span></span>
<span data-ttu-id="3b9ba-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-121">Database name.</span></span>

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

### <span data-ttu-id="3b9ba-122">-이름</span><span class="sxs-lookup"><span data-stu-id="3b9ba-122">-Name</span></span>
<span data-ttu-id="3b9ba-123">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="3b9ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b9ba-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3b9ba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9ba-126">-WhatIf</span></span>
<span data-ttu-id="3b9ba-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9ba-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b9ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9ba-129">CommonParameters</span></span>
<span data-ttu-id="3b9ba-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9ba-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9ba-132">입력</span><span class="sxs-lookup"><span data-stu-id="3b9ba-132">INPUTS</span></span>

### <span data-ttu-id="3b9ba-133">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="3b9ba-134">출력</span><span class="sxs-lookup"><span data-stu-id="3b9ba-134">OUTPUTS</span></span>

### <span data-ttu-id="3b9ba-135">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="3b9ba-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3b9ba-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3b9ba-136">NOTES</span></span>

## <span data-ttu-id="3b9ba-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b9ba-137">RELATED LINKS</span></span>
