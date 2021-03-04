---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a6808f6c2640a90006560b16dbfd452167e0d6fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971344"
---
# <span data-ttu-id="f504b-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="f504b-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="f504b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f504b-102">SYNOPSIS</span></span>
<span data-ttu-id="f504b-103">새 CosmosDB Sql Trigger를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f504b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f504b-104">SYNTAX</span></span>

### <span data-ttu-id="f504b-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f504b-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f504b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f504b-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f504b-107">설명</span><span class="sxs-lookup"><span data-stu-id="f504b-107">DESCRIPTION</span></span>
<span data-ttu-id="f504b-108">새 CosmosDB Sql Trigger를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="f504b-109">예제</span><span class="sxs-lookup"><span data-stu-id="f504b-109">EXAMPLES</span></span>

### <span data-ttu-id="f504b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f504b-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="f504b-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f504b-111">PARAMETERS</span></span>

### <span data-ttu-id="f504b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f504b-112">-AccountName</span></span>
<span data-ttu-id="f504b-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f504b-114">-Body</span><span class="sxs-lookup"><span data-stu-id="f504b-114">-Body</span></span>
<span data-ttu-id="f504b-115">트리거의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="f504b-116">-확인</span><span class="sxs-lookup"><span data-stu-id="f504b-116">-Confirm</span></span>
<span data-ttu-id="f504b-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f504b-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f504b-118">-ContainerName</span></span>
<span data-ttu-id="f504b-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-119">Container name.</span></span>

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

### <span data-ttu-id="f504b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f504b-120">-DatabaseName</span></span>
<span data-ttu-id="f504b-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-121">Database name.</span></span>

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

### <span data-ttu-id="f504b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f504b-122">-DefaultProfile</span></span>
<span data-ttu-id="f504b-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f504b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f504b-124">-Name</span></span>
<span data-ttu-id="f504b-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-125">Trigger name.</span></span>

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

### <span data-ttu-id="f504b-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f504b-126">-ParentObject</span></span>
<span data-ttu-id="f504b-127">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-127">Sql Container object.</span></span>

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

### <span data-ttu-id="f504b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f504b-128">-ResourceGroupName</span></span>
<span data-ttu-id="f504b-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="f504b-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="f504b-130">-TriggerOperation</span></span>
<span data-ttu-id="f504b-131">트리거가 연결된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="f504b-132">가능한 값은 다음과 같습니다. 'All', 'Create', 'Update', 'Delete', 'replace'</span><span class="sxs-lookup"><span data-stu-id="f504b-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="f504b-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="f504b-133">-TriggerType</span></span>
<span data-ttu-id="f504b-134">트리거의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-134">Type of the Trigger.</span></span>
<span data-ttu-id="f504b-135">가능한 값은 다음과 같습니다. 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="f504b-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="f504b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f504b-136">-WhatIf</span></span>
<span data-ttu-id="f504b-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f504b-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f504b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f504b-139">CommonParameters</span></span>
<span data-ttu-id="f504b-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f504b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f504b-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f504b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f504b-142">입력</span><span class="sxs-lookup"><span data-stu-id="f504b-142">INPUTS</span></span>

### <span data-ttu-id="f504b-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="f504b-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="f504b-144">출력</span><span class="sxs-lookup"><span data-stu-id="f504b-144">OUTPUTS</span></span>

### <span data-ttu-id="f504b-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f504b-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="f504b-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="f504b-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="f504b-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f504b-147">NOTES</span></span>

## <span data-ttu-id="f504b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f504b-148">RELATED LINKS</span></span>
