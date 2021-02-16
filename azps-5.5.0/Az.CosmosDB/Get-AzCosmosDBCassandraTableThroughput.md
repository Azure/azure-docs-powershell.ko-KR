---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199044"
---
# <span data-ttu-id="57575-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="57575-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="57575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57575-102">SYNOPSIS</span></span>
<span data-ttu-id="57575-103">Cassandra 테이블의 진행 값 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57575-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="57575-104">구문</span><span class="sxs-lookup"><span data-stu-id="57575-104">SYNTAX</span></span>

### <span data-ttu-id="57575-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="57575-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57575-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57575-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57575-107">설명</span><span class="sxs-lookup"><span data-stu-id="57575-107">DESCRIPTION</span></span>
<span data-ttu-id="57575-108">**Get-AzCosmosDBCassandraTableThroughput** cmdlet은 주어진 키스페이스에 해당하는 처리 시간 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57575-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="57575-109">예제</span><span class="sxs-lookup"><span data-stu-id="57575-109">EXAMPLES</span></span>

### <span data-ttu-id="57575-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="57575-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="57575-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57575-111">PARAMETERS</span></span>

### <span data-ttu-id="57575-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57575-112">-AccountName</span></span>
<span data-ttu-id="57575-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57575-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="57575-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57575-114">-Confirm</span></span>
<span data-ttu-id="57575-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57575-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57575-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57575-116">-DefaultProfile</span></span>
<span data-ttu-id="57575-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57575-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57575-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57575-118">-InputObject</span></span>
<span data-ttu-id="57575-119">Cassandra Table 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57575-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="57575-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="57575-120">-KeyspaceName</span></span>
<span data-ttu-id="57575-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57575-121">Database name.</span></span>

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

### <span data-ttu-id="57575-122">-Name</span><span class="sxs-lookup"><span data-stu-id="57575-122">-Name</span></span>
<span data-ttu-id="57575-123">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57575-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="57575-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57575-124">-ResourceGroupName</span></span>
<span data-ttu-id="57575-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57575-125">Name of resource group.</span></span>

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

### <span data-ttu-id="57575-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57575-126">-WhatIf</span></span>
<span data-ttu-id="57575-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57575-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57575-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57575-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57575-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57575-129">CommonParameters</span></span>
<span data-ttu-id="57575-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57575-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57575-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57575-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57575-132">입력</span><span class="sxs-lookup"><span data-stu-id="57575-132">INPUTS</span></span>

### <span data-ttu-id="57575-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="57575-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="57575-134">출력</span><span class="sxs-lookup"><span data-stu-id="57575-134">OUTPUTS</span></span>

### <span data-ttu-id="57575-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="57575-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="57575-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57575-136">NOTES</span></span>

## <span data-ttu-id="57575-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57575-137">RELATED LINKS</span></span>
