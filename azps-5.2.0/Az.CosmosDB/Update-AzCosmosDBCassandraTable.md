---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344654"
---
# <span data-ttu-id="eca33-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="eca33-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="eca33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca33-102">SYNOPSIS</span></span>
<span data-ttu-id="eca33-103">CosmosDB Cassandra 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="eca33-104">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="eca33-105">구문</span><span class="sxs-lookup"><span data-stu-id="eca33-105">SYNTAX</span></span>

### <span data-ttu-id="eca33-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="eca33-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca33-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca33-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eca33-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca33-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eca33-109">설명</span><span class="sxs-lookup"><span data-stu-id="eca33-109">DESCRIPTION</span></span>
<span data-ttu-id="eca33-110">CosmosDB Cassandra 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="eca33-111">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="eca33-112">예제</span><span class="sxs-lookup"><span data-stu-id="eca33-112">EXAMPLES</span></span>

### <span data-ttu-id="eca33-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="eca33-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="eca33-114">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="eca33-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="eca33-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eca33-115">PARAMETERS</span></span>

### <span data-ttu-id="eca33-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eca33-116">-AccountName</span></span>
<span data-ttu-id="eca33-117">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eca33-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="eca33-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="eca33-119">분석 저장소 TTL입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="eca33-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="eca33-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="eca33-121">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="eca33-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eca33-122">-Confirm</span></span>
<span data-ttu-id="eca33-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca33-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca33-124">-DefaultProfile</span></span>
<span data-ttu-id="eca33-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca33-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eca33-126">-InputObject</span></span>
<span data-ttu-id="eca33-127">Cassandra Table 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-127">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eca33-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="eca33-128">-KeyspaceName</span></span>
<span data-ttu-id="eca33-129">Cassandra Keyspace 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="eca33-130">-Name</span><span class="sxs-lookup"><span data-stu-id="eca33-130">-Name</span></span>
<span data-ttu-id="eca33-131">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="eca33-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eca33-132">-ParentObject</span></span>
<span data-ttu-id="eca33-133">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="eca33-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca33-134">-ResourceGroupName</span></span>
<span data-ttu-id="eca33-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-135">Name of resource group.</span></span>

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

### <span data-ttu-id="eca33-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="eca33-136">-Schema</span></span>
<span data-ttu-id="eca33-137">PSCassandraSchema 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="eca33-138">이 New-AzCosmosDBCassandraSchema 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eca33-139">-Throughput</span><span class="sxs-lookup"><span data-stu-id="eca33-139">-Throughput</span></span>
<span data-ttu-id="eca33-140">Cassandra Keyspace(RU/s)의 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="eca33-141">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-141">Default value is 400.</span></span>

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

### <span data-ttu-id="eca33-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="eca33-142">-TtlInSeconds</span></span>
<span data-ttu-id="eca33-143">기본 Ttl(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="eca33-144">값이 누락되었거나 - 1로 설정된 경우 항목이 만료되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="eca33-145">값이 n로 설정된 경우 항목은 마지막으로 수정된 시간 이후 n초 후에 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="eca33-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca33-146">-WhatIf</span></span>
<span data-ttu-id="eca33-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eca33-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca33-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca33-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca33-149">CommonParameters</span></span>
<span data-ttu-id="eca33-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eca33-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca33-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eca33-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca33-152">입력</span><span class="sxs-lookup"><span data-stu-id="eca33-152">INPUTS</span></span>

### <span data-ttu-id="eca33-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="eca33-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="eca33-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="eca33-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="eca33-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="eca33-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="eca33-156">출력</span><span class="sxs-lookup"><span data-stu-id="eca33-156">OUTPUTS</span></span>

### <span data-ttu-id="eca33-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="eca33-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="eca33-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="eca33-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="eca33-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eca33-159">NOTES</span></span>

## <span data-ttu-id="eca33-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eca33-160">RELATED LINKS</span></span>
