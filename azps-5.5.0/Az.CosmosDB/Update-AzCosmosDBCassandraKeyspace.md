---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177220"
---
# <span data-ttu-id="e54e9-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="e54e9-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="e54e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e54e9-103">CosmosDB Cassandra Keyspace를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="e54e9-104">기존 Keyspace를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="e54e9-105">구문</span><span class="sxs-lookup"><span data-stu-id="e54e9-105">SYNTAX</span></span>

### <span data-ttu-id="e54e9-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e54e9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e54e9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e54e9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e54e9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e54e9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e54e9-109">설명</span><span class="sxs-lookup"><span data-stu-id="e54e9-109">DESCRIPTION</span></span>
<span data-ttu-id="e54e9-110">CosmosDB Cassandra Keyspace를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="e54e9-111">기존 Keyspace를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="e54e9-112">예제</span><span class="sxs-lookup"><span data-stu-id="e54e9-112">EXAMPLES</span></span>

### <span data-ttu-id="e54e9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="e54e9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="e54e9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e54e9-114">PARAMETERS</span></span>

### <span data-ttu-id="e54e9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e54e9-115">-AccountName</span></span>
<span data-ttu-id="e54e9-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e54e9-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e54e9-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e54e9-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e54e9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e54e9-119">-Confirm</span></span>
<span data-ttu-id="e54e9-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e54e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54e9-121">-DefaultProfile</span></span>
<span data-ttu-id="e54e9-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e54e9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e54e9-123">-InputObject</span></span>
<span data-ttu-id="e54e9-124">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-124">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e54e9-125">-Name</span></span>
<span data-ttu-id="e54e9-126">Cassandra 키스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e54e9-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e54e9-127">-ParentObject</span></span>
<span data-ttu-id="e54e9-128">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="e54e9-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e54e9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54e9-129">-ResourceGroupName</span></span>
<span data-ttu-id="e54e9-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-130">Name of resource group.</span></span>

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

### <span data-ttu-id="e54e9-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="e54e9-131">-Throughput</span></span>
<span data-ttu-id="e54e9-132">Cassandra Keyspace(RU/s)의 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="e54e9-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-133">Default value is 400.</span></span>

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

### <span data-ttu-id="e54e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e54e9-134">-WhatIf</span></span>
<span data-ttu-id="e54e9-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e54e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e54e9-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e54e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54e9-137">CommonParameters</span></span>
<span data-ttu-id="e54e9-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e54e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54e9-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e54e9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54e9-140">입력</span><span class="sxs-lookup"><span data-stu-id="e54e9-140">INPUTS</span></span>

### <span data-ttu-id="e54e9-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e54e9-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="e54e9-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e54e9-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e54e9-143">출력</span><span class="sxs-lookup"><span data-stu-id="e54e9-143">OUTPUTS</span></span>

### <span data-ttu-id="e54e9-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e54e9-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="e54e9-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e54e9-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e54e9-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e54e9-146">NOTES</span></span>

## <span data-ttu-id="e54e9-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e54e9-147">RELATED LINKS</span></span>
