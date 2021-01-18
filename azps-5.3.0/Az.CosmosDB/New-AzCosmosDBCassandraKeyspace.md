---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495802"
---
# <span data-ttu-id="a47ab-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="a47ab-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="a47ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a47ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a47ab-103">새 CosmosDB Cassandra 키스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a47ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="a47ab-104">SYNTAX</span></span>

### <span data-ttu-id="a47ab-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a47ab-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47ab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a47ab-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a47ab-107">설명</span><span class="sxs-lookup"><span data-stu-id="a47ab-107">DESCRIPTION</span></span>
<span data-ttu-id="a47ab-108">새 CosmosDB Cassandra 키스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="a47ab-109">예제</span><span class="sxs-lookup"><span data-stu-id="a47ab-109">EXAMPLES</span></span>

### <span data-ttu-id="a47ab-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a47ab-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="a47ab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a47ab-111">PARAMETERS</span></span>

### <span data-ttu-id="a47ab-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a47ab-112">-AccountName</span></span>
<span data-ttu-id="a47ab-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a47ab-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a47ab-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a47ab-115">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a47ab-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a47ab-116">-Confirm</span></span>
<span data-ttu-id="a47ab-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47ab-118">-DefaultProfile</span></span>
<span data-ttu-id="a47ab-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a47ab-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a47ab-120">-Name</span></span>
<span data-ttu-id="a47ab-121">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-121">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47ab-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a47ab-122">-ParentObject</span></span>
<span data-ttu-id="a47ab-123">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="a47ab-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="a47ab-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a47ab-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="a47ab-126">-Throughput</span></span>
<span data-ttu-id="a47ab-127">Cassandra Keyspace(RU/s)의 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="a47ab-128">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-128">Default value is 400.</span></span>

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

### <span data-ttu-id="a47ab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47ab-129">-WhatIf</span></span>
<span data-ttu-id="a47ab-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a47ab-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a47ab-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47ab-132">CommonParameters</span></span>
<span data-ttu-id="a47ab-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a47ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47ab-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a47ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47ab-135">입력</span><span class="sxs-lookup"><span data-stu-id="a47ab-135">INPUTS</span></span>

### <span data-ttu-id="a47ab-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a47ab-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a47ab-137">출력</span><span class="sxs-lookup"><span data-stu-id="a47ab-137">OUTPUTS</span></span>

### <span data-ttu-id="a47ab-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="a47ab-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="a47ab-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="a47ab-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="a47ab-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a47ab-140">NOTES</span></span>

## <span data-ttu-id="a47ab-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a47ab-141">RELATED LINKS</span></span>
