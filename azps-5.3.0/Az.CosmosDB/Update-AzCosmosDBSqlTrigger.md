---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493641"
---
# <span data-ttu-id="abc67-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="abc67-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="abc67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abc67-102">SYNOPSIS</span></span>
<span data-ttu-id="abc67-103">CosmosDB Sql 트리거를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="abc67-104">기존 트리거를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="abc67-105">구문</span><span class="sxs-lookup"><span data-stu-id="abc67-105">SYNTAX</span></span>

### <span data-ttu-id="abc67-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="abc67-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc67-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abc67-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc67-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abc67-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc67-109">설명</span><span class="sxs-lookup"><span data-stu-id="abc67-109">DESCRIPTION</span></span>
<span data-ttu-id="abc67-110">CosmosDB Sql 트리거를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="abc67-111">기존 트리거를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="abc67-112">예제</span><span class="sxs-lookup"><span data-stu-id="abc67-112">EXAMPLES</span></span>

### <span data-ttu-id="abc67-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="abc67-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="abc67-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abc67-114">PARAMETERS</span></span>

### <span data-ttu-id="abc67-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="abc67-115">-AccountName</span></span>
<span data-ttu-id="abc67-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="abc67-117">-Body</span><span class="sxs-lookup"><span data-stu-id="abc67-117">-Body</span></span>
<span data-ttu-id="abc67-118">트리거의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="abc67-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abc67-119">-Confirm</span></span>
<span data-ttu-id="abc67-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc67-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="abc67-121">-ContainerName</span></span>
<span data-ttu-id="abc67-122">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-122">Container name.</span></span>

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

### <span data-ttu-id="abc67-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="abc67-123">-DatabaseName</span></span>
<span data-ttu-id="abc67-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-124">Database name.</span></span>

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

### <span data-ttu-id="abc67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc67-125">-DefaultProfile</span></span>
<span data-ttu-id="abc67-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abc67-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abc67-127">-InputObject</span></span>
<span data-ttu-id="abc67-128">Sql 트리거 개체</span><span class="sxs-lookup"><span data-stu-id="abc67-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abc67-129">-Name</span><span class="sxs-lookup"><span data-stu-id="abc67-129">-Name</span></span>
<span data-ttu-id="abc67-130">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-130">Trigger name.</span></span>

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

### <span data-ttu-id="abc67-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="abc67-131">-ParentObject</span></span>
<span data-ttu-id="abc67-132">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-132">Sql Container object.</span></span>

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

### <span data-ttu-id="abc67-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc67-133">-ResourceGroupName</span></span>
<span data-ttu-id="abc67-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-134">Name of resource group.</span></span>

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

### <span data-ttu-id="abc67-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="abc67-135">-TriggerOperation</span></span>
<span data-ttu-id="abc67-136">트리거가 연결된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="abc67-137">가능한 값은 'All', 'Create', 'Update', 'Delete', 'Replace'입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="abc67-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="abc67-138">-TriggerType</span></span>
<span data-ttu-id="abc67-139">트리거의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-139">Type of the Trigger.</span></span>
<span data-ttu-id="abc67-140">가능한 값은 'Pre', 'Post'입니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="abc67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc67-141">-WhatIf</span></span>
<span data-ttu-id="abc67-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="abc67-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc67-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc67-144">CommonParameters</span></span>
<span data-ttu-id="abc67-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="abc67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc67-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="abc67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc67-147">입력</span><span class="sxs-lookup"><span data-stu-id="abc67-147">INPUTS</span></span>

### <span data-ttu-id="abc67-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="abc67-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="abc67-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="abc67-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="abc67-150">출력</span><span class="sxs-lookup"><span data-stu-id="abc67-150">OUTPUTS</span></span>

### <span data-ttu-id="abc67-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="abc67-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="abc67-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="abc67-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="abc67-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="abc67-153">NOTES</span></span>

## <span data-ttu-id="abc67-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abc67-154">RELATED LINKS</span></span>
