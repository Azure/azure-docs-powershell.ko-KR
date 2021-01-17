---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372968"
---
# <span data-ttu-id="81fd6-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81fd6-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="81fd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="81fd6-103">CosmosDB Sql Database를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="81fd6-104">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="81fd6-105">구문</span><span class="sxs-lookup"><span data-stu-id="81fd6-105">SYNTAX</span></span>

### <span data-ttu-id="81fd6-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="81fd6-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81fd6-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81fd6-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81fd6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81fd6-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81fd6-109">설명</span><span class="sxs-lookup"><span data-stu-id="81fd6-109">DESCRIPTION</span></span>
<span data-ttu-id="81fd6-110">CosmosDB Sql Database를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="81fd6-111">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="81fd6-112">예제</span><span class="sxs-lookup"><span data-stu-id="81fd6-112">EXAMPLES</span></span>

### <span data-ttu-id="81fd6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="81fd6-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="81fd6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81fd6-114">PARAMETERS</span></span>

### <span data-ttu-id="81fd6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="81fd6-115">-AccountName</span></span>
<span data-ttu-id="81fd6-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81fd6-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="81fd6-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="81fd6-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="81fd6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81fd6-119">-Confirm</span></span>
<span data-ttu-id="81fd6-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81fd6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fd6-121">-DefaultProfile</span></span>
<span data-ttu-id="81fd6-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81fd6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81fd6-123">-InputObject</span></span>
<span data-ttu-id="81fd6-124">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-124">Sql Database object.</span></span>

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

### <span data-ttu-id="81fd6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="81fd6-125">-Name</span></span>
<span data-ttu-id="81fd6-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-126">Database name.</span></span>

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

### <span data-ttu-id="81fd6-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81fd6-127">-ParentObject</span></span>
<span data-ttu-id="81fd6-128">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="81fd6-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="81fd6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81fd6-129">-ResourceGroupName</span></span>
<span data-ttu-id="81fd6-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-130">Name of resource group.</span></span>

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

### <span data-ttu-id="81fd6-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="81fd6-131">-Throughput</span></span>
<span data-ttu-id="81fd6-132">데이터베이스의 SQL(RU/s)</span><span class="sxs-lookup"><span data-stu-id="81fd6-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="81fd6-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-133">Default value is 400.</span></span>

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

### <span data-ttu-id="81fd6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81fd6-134">-WhatIf</span></span>
<span data-ttu-id="81fd6-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="81fd6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81fd6-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81fd6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fd6-137">CommonParameters</span></span>
<span data-ttu-id="81fd6-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81fd6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fd6-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81fd6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fd6-140">입력</span><span class="sxs-lookup"><span data-stu-id="81fd6-140">INPUTS</span></span>

### <span data-ttu-id="81fd6-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="81fd6-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="81fd6-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="81fd6-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="81fd6-143">출력</span><span class="sxs-lookup"><span data-stu-id="81fd6-143">OUTPUTS</span></span>

### <span data-ttu-id="81fd6-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="81fd6-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="81fd6-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="81fd6-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="81fd6-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81fd6-146">NOTES</span></span>

## <span data-ttu-id="81fd6-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81fd6-147">RELATED LINKS</span></span>
