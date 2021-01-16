---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363154"
---
# <span data-ttu-id="da05e-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="da05e-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="da05e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da05e-102">SYNOPSIS</span></span>
<span data-ttu-id="da05e-103">CosmosDB MongoDB 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="da05e-104">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="da05e-105">구문</span><span class="sxs-lookup"><span data-stu-id="da05e-105">SYNTAX</span></span>

### <span data-ttu-id="da05e-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="da05e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da05e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da05e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da05e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da05e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da05e-109">설명</span><span class="sxs-lookup"><span data-stu-id="da05e-109">DESCRIPTION</span></span>
<span data-ttu-id="da05e-110">CosmosDB MongoDB 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="da05e-111">기존 데이터베이스를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="da05e-112">예제</span><span class="sxs-lookup"><span data-stu-id="da05e-112">EXAMPLES</span></span>

### <span data-ttu-id="da05e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="da05e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="da05e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da05e-114">PARAMETERS</span></span>

### <span data-ttu-id="da05e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da05e-115">-AccountName</span></span>
<span data-ttu-id="da05e-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="da05e-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="da05e-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="da05e-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="da05e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da05e-119">-Confirm</span></span>
<span data-ttu-id="da05e-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da05e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da05e-121">-DefaultProfile</span></span>
<span data-ttu-id="da05e-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da05e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da05e-123">-InputObject</span></span>
<span data-ttu-id="da05e-124">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da05e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="da05e-125">-Name</span></span>
<span data-ttu-id="da05e-126">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-126">Database name.</span></span>

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

### <span data-ttu-id="da05e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="da05e-127">-ParentObject</span></span>
<span data-ttu-id="da05e-128">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="da05e-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da05e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da05e-129">-ResourceGroupName</span></span>
<span data-ttu-id="da05e-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="da05e-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="da05e-131">-Throughput</span></span>
<span data-ttu-id="da05e-132">Mongo 데이터베이스(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="da05e-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-133">Default value is 400.</span></span>

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

### <span data-ttu-id="da05e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da05e-134">-WhatIf</span></span>
<span data-ttu-id="da05e-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da05e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da05e-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da05e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da05e-137">CommonParameters</span></span>
<span data-ttu-id="da05e-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da05e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da05e-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da05e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da05e-140">입력</span><span class="sxs-lookup"><span data-stu-id="da05e-140">INPUTS</span></span>

### <span data-ttu-id="da05e-141">없음</span><span class="sxs-lookup"><span data-stu-id="da05e-141">None</span></span>

## <span data-ttu-id="da05e-142">출력</span><span class="sxs-lookup"><span data-stu-id="da05e-142">OUTPUTS</span></span>

### <span data-ttu-id="da05e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="da05e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="da05e-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="da05e-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="da05e-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da05e-145">NOTES</span></span>

## <span data-ttu-id="da05e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da05e-146">RELATED LINKS</span></span>
