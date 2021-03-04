---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 23e4ed96f464d29e95bacd04b93326cb5ce8e3da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977179"
---
# <span data-ttu-id="d09d3-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="d09d3-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="d09d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d09d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d09d3-103">CosmosDB Sql Database의 처리당 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d09d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="d09d3-104">SYNTAX</span></span>

### <span data-ttu-id="d09d3-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d09d3-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d09d3-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d09d3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d09d3-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d09d3-108">설명</span><span class="sxs-lookup"><span data-stu-id="d09d3-108">DESCRIPTION</span></span>
<span data-ttu-id="d09d3-109">CosmosDB Sql Database의 처리당 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="d09d3-110">예제</span><span class="sxs-lookup"><span data-stu-id="d09d3-110">EXAMPLES</span></span>

### <span data-ttu-id="d09d3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d09d3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d09d3-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d09d3-112">PARAMETERS</span></span>

### <span data-ttu-id="d09d3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d09d3-113">-AccountName</span></span>
<span data-ttu-id="d09d3-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d09d3-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d09d3-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d09d3-116">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d09d3-117">-확인</span><span class="sxs-lookup"><span data-stu-id="d09d3-117">-Confirm</span></span>
<span data-ttu-id="d09d3-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d09d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d09d3-119">-DefaultProfile</span></span>
<span data-ttu-id="d09d3-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d09d3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d09d3-121">-InputObject</span></span>
<span data-ttu-id="d09d3-122">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d09d3-122">CosmosDB Account object</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d09d3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d09d3-123">-Name</span></span>
<span data-ttu-id="d09d3-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-124">Database name.</span></span>

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

### <span data-ttu-id="d09d3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d09d3-125">-ParentObject</span></span>
<span data-ttu-id="d09d3-126">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d09d3-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d09d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d09d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="d09d3-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d09d3-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="d09d3-129">-Throughput</span></span>
<span data-ttu-id="d09d3-130">RU/s의 SQL().입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="d09d3-131">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-131">Default value is 400.</span></span>

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

### <span data-ttu-id="d09d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d09d3-132">-WhatIf</span></span>
<span data-ttu-id="d09d3-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d09d3-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d09d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09d3-135">CommonParameters</span></span>
<span data-ttu-id="d09d3-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d09d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09d3-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d09d3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09d3-138">입력</span><span class="sxs-lookup"><span data-stu-id="d09d3-138">INPUTS</span></span>

### <span data-ttu-id="d09d3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d09d3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d09d3-140">출력</span><span class="sxs-lookup"><span data-stu-id="d09d3-140">OUTPUTS</span></span>

### <span data-ttu-id="d09d3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d09d3-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d09d3-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d09d3-142">NOTES</span></span>

## <span data-ttu-id="d09d3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d09d3-143">RELATED LINKS</span></span>
