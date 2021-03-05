---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: a223fd71ecf65ecb34b605e79ee0d6f7670d3a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977360"
---
# <span data-ttu-id="78dd8-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="78dd8-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="78dd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="78dd8-103">CosmosDB Gremlin 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="78dd8-104">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="78dd8-105">구문</span><span class="sxs-lookup"><span data-stu-id="78dd8-105">SYNTAX</span></span>

### <span data-ttu-id="78dd8-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="78dd8-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78dd8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78dd8-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78dd8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78dd8-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78dd8-109">설명</span><span class="sxs-lookup"><span data-stu-id="78dd8-109">DESCRIPTION</span></span>
<span data-ttu-id="78dd8-110">CosmosDB Gremlin 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="78dd8-111">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="78dd8-112">예제</span><span class="sxs-lookup"><span data-stu-id="78dd8-112">EXAMPLES</span></span>

### <span data-ttu-id="78dd8-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="78dd8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="78dd8-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="78dd8-114">PARAMETERS</span></span>

### <span data-ttu-id="78dd8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78dd8-115">-AccountName</span></span>
<span data-ttu-id="78dd8-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="78dd8-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="78dd8-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="78dd8-118">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="78dd8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="78dd8-119">-Confirm</span></span>
<span data-ttu-id="78dd8-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78dd8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78dd8-121">-DefaultProfile</span></span>
<span data-ttu-id="78dd8-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78dd8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78dd8-123">-InputObject</span></span>
<span data-ttu-id="78dd8-124">Gremlin Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="78dd8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="78dd8-125">-Name</span></span>
<span data-ttu-id="78dd8-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-126">Database name.</span></span>

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

### <span data-ttu-id="78dd8-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78dd8-127">-ParentObject</span></span>
<span data-ttu-id="78dd8-128">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="78dd8-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="78dd8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78dd8-129">-ResourceGroupName</span></span>
<span data-ttu-id="78dd8-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-130">Name of resource group.</span></span>

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

### <span data-ttu-id="78dd8-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="78dd8-131">-Throughput</span></span>
<span data-ttu-id="78dd8-132">Gremlin Database(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="78dd8-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-133">Default value is 400.</span></span>

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

### <span data-ttu-id="78dd8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78dd8-134">-WhatIf</span></span>
<span data-ttu-id="78dd8-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78dd8-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78dd8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78dd8-137">CommonParameters</span></span>
<span data-ttu-id="78dd8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78dd8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78dd8-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78dd8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78dd8-140">입력</span><span class="sxs-lookup"><span data-stu-id="78dd8-140">INPUTS</span></span>

### <span data-ttu-id="78dd8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="78dd8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="78dd8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78dd8-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="78dd8-143">출력</span><span class="sxs-lookup"><span data-stu-id="78dd8-143">OUTPUTS</span></span>

### <span data-ttu-id="78dd8-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78dd8-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="78dd8-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="78dd8-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="78dd8-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78dd8-146">NOTES</span></span>

## <span data-ttu-id="78dd8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78dd8-147">RELATED LINKS</span></span>
