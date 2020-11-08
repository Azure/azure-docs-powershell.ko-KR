---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214608"
---
# <span data-ttu-id="9de78-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="9de78-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="9de78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de78-102">SYNOPSIS</span></span>
<span data-ttu-id="9de78-103">CosmosDB Cassandra 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="9de78-104">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="9de78-105">구문과</span><span class="sxs-lookup"><span data-stu-id="9de78-105">SYNTAX</span></span>

### <span data-ttu-id="9de78-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9de78-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de78-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de78-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9de78-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de78-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9de78-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9de78-109">DESCRIPTION</span></span>
<span data-ttu-id="9de78-110">CosmosDB Cassandra 테이블을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="9de78-111">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="9de78-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9de78-112">EXAMPLES</span></span>

### <span data-ttu-id="9de78-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9de78-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="9de78-114">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="9de78-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="9de78-115">변수</span><span class="sxs-lookup"><span data-stu-id="9de78-115">PARAMETERS</span></span>

### <span data-ttu-id="9de78-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9de78-116">-AccountName</span></span>
<span data-ttu-id="9de78-117">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9de78-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="9de78-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="9de78-119">분석 저장소 TTL.</span><span class="sxs-lookup"><span data-stu-id="9de78-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="9de78-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="9de78-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="9de78-121">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="9de78-122">-확인</span><span class="sxs-lookup"><span data-stu-id="9de78-122">-Confirm</span></span>
<span data-ttu-id="9de78-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de78-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de78-124">-DefaultProfile</span></span>
<span data-ttu-id="9de78-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de78-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9de78-126">-InputObject</span></span>
<span data-ttu-id="9de78-127">Cassandra Table 개체</span><span class="sxs-lookup"><span data-stu-id="9de78-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="9de78-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="9de78-128">-KeyspaceName</span></span>
<span data-ttu-id="9de78-129">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="9de78-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9de78-130">-이름</span><span class="sxs-lookup"><span data-stu-id="9de78-130">-Name</span></span>
<span data-ttu-id="9de78-131">Cassandra 테이블 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="9de78-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9de78-132">-ParentObject</span></span>
<span data-ttu-id="9de78-133">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9de78-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de78-134">-ResourceGroupName</span></span>
<span data-ttu-id="9de78-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-135">Name of resource group.</span></span>

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

### <span data-ttu-id="9de78-136">-스키마</span><span class="sxs-lookup"><span data-stu-id="9de78-136">-Schema</span></span>
<span data-ttu-id="9de78-137">PSCassandraSchema 개체</span><span class="sxs-lookup"><span data-stu-id="9de78-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="9de78-138">이 개체를 만들려면 New-AzCosmosDBCassandraSchema를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="9de78-139">-처리량</span><span class="sxs-lookup"><span data-stu-id="9de78-139">-Throughput</span></span>
<span data-ttu-id="9de78-140">Cassandra Keyspace (a r/s)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9de78-141">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-141">Default value is 400.</span></span>

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

### <span data-ttu-id="9de78-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="9de78-142">-TtlInSeconds</span></span>
<span data-ttu-id="9de78-143">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="9de78-144">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="9de78-145">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="9de78-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de78-146">-WhatIf</span></span>
<span data-ttu-id="9de78-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de78-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de78-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de78-149">CommonParameters</span></span>
<span data-ttu-id="9de78-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9de78-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de78-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9de78-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de78-152">입력</span><span class="sxs-lookup"><span data-stu-id="9de78-152">INPUTS</span></span>

### <span data-ttu-id="9de78-153">CosmosDB. PSCassandraSchema/.</span><span class="sxs-lookup"><span data-stu-id="9de78-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="9de78-154">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9de78-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="9de78-155">CosmosDB. PSCassandraTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9de78-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="9de78-156">출력</span><span class="sxs-lookup"><span data-stu-id="9de78-156">OUTPUTS</span></span>

### <span data-ttu-id="9de78-157">CosmosDB. PSCassandraTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9de78-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="9de78-158">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="9de78-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9de78-159">상속자</span><span class="sxs-lookup"><span data-stu-id="9de78-159">NOTES</span></span>

## <span data-ttu-id="9de78-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9de78-160">RELATED LINKS</span></span>
