---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214199"
---
# <span data-ttu-id="c8d24-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c8d24-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="c8d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d24-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d24-103">이를 사용 하 여 자동 크기 조정 처리량을 수동 처리량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c8d24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8d24-104">SYNTAX</span></span>

### <span data-ttu-id="c8d24-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c8d24-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8d24-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d24-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d24-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d24-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d24-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c8d24-108">DESCRIPTION</span></span>
<span data-ttu-id="c8d24-109">ThroughpyteType 매개 변수는 마이그레이션할 처리량을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c8d24-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c8d24-110">EXAMPLES</span></span>

### <span data-ttu-id="c8d24-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8d24-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="c8d24-112">변수</span><span class="sxs-lookup"><span data-stu-id="c8d24-112">PARAMETERS</span></span>

### <span data-ttu-id="c8d24-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c8d24-113">-AccountName</span></span>
<span data-ttu-id="c8d24-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c8d24-115">-확인</span><span class="sxs-lookup"><span data-stu-id="c8d24-115">-Confirm</span></span>
<span data-ttu-id="c8d24-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d24-117">-DefaultProfile</span></span>
<span data-ttu-id="c8d24-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8d24-119">-InputObject</span></span>
<span data-ttu-id="c8d24-120">Cassandra Keyspace 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c8d24-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c8d24-121">-Name</span></span>
<span data-ttu-id="c8d24-122">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="c8d24-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c8d24-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c8d24-123">-ParentObject</span></span>
<span data-ttu-id="c8d24-124">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="c8d24-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c8d24-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d24-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8d24-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-126">Name of resource group.</span></span>

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

### <span data-ttu-id="c8d24-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="c8d24-127">-ThroughputType</span></span>
<span data-ttu-id="c8d24-128">마이그레이션할 처리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="c8d24-129">사용할 수 있는 값은 자동 크기 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c8d24-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d24-130">-WhatIf</span></span>
<span data-ttu-id="c8d24-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d24-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d24-133">CommonParameters</span></span>
<span data-ttu-id="c8d24-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d24-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c8d24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d24-136">입력</span><span class="sxs-lookup"><span data-stu-id="c8d24-136">INPUTS</span></span>

### <span data-ttu-id="c8d24-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="c8d24-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="c8d24-138">CosmosDB. PSCassandraKeyspaceGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c8d24-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c8d24-139">출력</span><span class="sxs-lookup"><span data-stu-id="c8d24-139">OUTPUTS</span></span>

### <span data-ttu-id="c8d24-140">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c8d24-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c8d24-141">상속자</span><span class="sxs-lookup"><span data-stu-id="c8d24-141">NOTES</span></span>

## <span data-ttu-id="c8d24-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8d24-142">RELATED LINKS</span></span>
