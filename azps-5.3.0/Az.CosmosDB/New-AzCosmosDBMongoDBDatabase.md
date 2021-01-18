---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493690"
---
# <span data-ttu-id="5e9d9-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="5e9d9-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="5e9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9d9-103">새 CosmosDB MongoDB 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="5e9d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e9d9-104">SYNTAX</span></span>

### <span data-ttu-id="5e9d9-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5e9d9-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e9d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e9d9-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e9d9-107">설명</span><span class="sxs-lookup"><span data-stu-id="5e9d9-107">DESCRIPTION</span></span>
<span data-ttu-id="5e9d9-108">새 CosmosDB MongoDB 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="5e9d9-109">예제</span><span class="sxs-lookup"><span data-stu-id="5e9d9-109">EXAMPLES</span></span>

### <span data-ttu-id="5e9d9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5e9d9-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="5e9d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e9d9-111">PARAMETERS</span></span>

### <span data-ttu-id="5e9d9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e9d9-112">-AccountName</span></span>
<span data-ttu-id="5e9d9-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e9d9-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5e9d9-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5e9d9-115">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5e9d9-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e9d9-116">-Confirm</span></span>
<span data-ttu-id="5e9d9-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e9d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9d9-118">-DefaultProfile</span></span>
<span data-ttu-id="5e9d9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e9d9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5e9d9-120">-Name</span></span>
<span data-ttu-id="5e9d9-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-121">Database name.</span></span>

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

### <span data-ttu-id="5e9d9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e9d9-122">-ParentObject</span></span>
<span data-ttu-id="5e9d9-123">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="5e9d9-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5e9d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e9d9-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5e9d9-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="5e9d9-126">-Throughput</span></span>
<span data-ttu-id="5e9d9-127">Mongo 데이터베이스(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="5e9d9-128">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-128">Default value is 400.</span></span>

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

### <span data-ttu-id="5e9d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e9d9-129">-WhatIf</span></span>
<span data-ttu-id="5e9d9-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5e9d9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e9d9-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e9d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9d9-132">CommonParameters</span></span>
<span data-ttu-id="5e9d9-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9d9-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9d9-135">입력</span><span class="sxs-lookup"><span data-stu-id="5e9d9-135">INPUTS</span></span>

### <span data-ttu-id="5e9d9-136">없음</span><span class="sxs-lookup"><span data-stu-id="5e9d9-136">None</span></span>

## <span data-ttu-id="5e9d9-137">출력</span><span class="sxs-lookup"><span data-stu-id="5e9d9-137">OUTPUTS</span></span>

### <span data-ttu-id="5e9d9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5e9d9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="5e9d9-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5e9d9-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5e9d9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e9d9-140">NOTES</span></span>

## <span data-ttu-id="5e9d9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e9d9-141">RELATED LINKS</span></span>
