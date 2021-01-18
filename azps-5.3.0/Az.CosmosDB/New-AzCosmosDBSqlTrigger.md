---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495778"
---
# <span data-ttu-id="36765-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="36765-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="36765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36765-102">SYNOPSIS</span></span>
<span data-ttu-id="36765-103">새 CosmosDB Sql 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36765-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="36765-104">구문</span><span class="sxs-lookup"><span data-stu-id="36765-104">SYNTAX</span></span>

### <span data-ttu-id="36765-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="36765-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36765-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36765-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36765-107">설명</span><span class="sxs-lookup"><span data-stu-id="36765-107">DESCRIPTION</span></span>
<span data-ttu-id="36765-108">새 CosmosDB Sql 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36765-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="36765-109">예제</span><span class="sxs-lookup"><span data-stu-id="36765-109">EXAMPLES</span></span>

### <span data-ttu-id="36765-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="36765-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="36765-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36765-111">PARAMETERS</span></span>

### <span data-ttu-id="36765-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36765-112">-AccountName</span></span>
<span data-ttu-id="36765-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36765-114">-Body</span><span class="sxs-lookup"><span data-stu-id="36765-114">-Body</span></span>
<span data-ttu-id="36765-115">트리거의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="36765-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36765-116">-Confirm</span></span>
<span data-ttu-id="36765-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36765-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36765-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="36765-118">-ContainerName</span></span>
<span data-ttu-id="36765-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-119">Container name.</span></span>

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

### <span data-ttu-id="36765-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36765-120">-DatabaseName</span></span>
<span data-ttu-id="36765-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-121">Database name.</span></span>

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

### <span data-ttu-id="36765-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36765-122">-DefaultProfile</span></span>
<span data-ttu-id="36765-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36765-124">-Name</span><span class="sxs-lookup"><span data-stu-id="36765-124">-Name</span></span>
<span data-ttu-id="36765-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-125">Trigger name.</span></span>

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

### <span data-ttu-id="36765-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36765-126">-ParentObject</span></span>
<span data-ttu-id="36765-127">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-127">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36765-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36765-128">-ResourceGroupName</span></span>
<span data-ttu-id="36765-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-129">Name of resource group.</span></span>

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

### <span data-ttu-id="36765-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="36765-130">-TriggerOperation</span></span>
<span data-ttu-id="36765-131">트리거가 연결된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="36765-132">가능한 값은 'All', 'Create', 'Update', 'Delete', 'Replace'입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="36765-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="36765-133">-TriggerType</span></span>
<span data-ttu-id="36765-134">트리거의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-134">Type of the Trigger.</span></span>
<span data-ttu-id="36765-135">가능한 값은 'Pre', 'Post'입니다.</span><span class="sxs-lookup"><span data-stu-id="36765-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="36765-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36765-136">-WhatIf</span></span>
<span data-ttu-id="36765-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="36765-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36765-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36765-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36765-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36765-139">CommonParameters</span></span>
<span data-ttu-id="36765-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36765-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36765-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36765-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36765-142">입력</span><span class="sxs-lookup"><span data-stu-id="36765-142">INPUTS</span></span>

### <span data-ttu-id="36765-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="36765-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="36765-144">출력</span><span class="sxs-lookup"><span data-stu-id="36765-144">OUTPUTS</span></span>

### <span data-ttu-id="36765-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="36765-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="36765-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="36765-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="36765-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36765-147">NOTES</span></span>

## <span data-ttu-id="36765-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36765-148">RELATED LINKS</span></span>
