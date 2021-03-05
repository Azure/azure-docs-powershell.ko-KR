---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: bebf801316d18b29f6444b0b369833ae547e78d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009728"
---
# <span data-ttu-id="aa58a-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="aa58a-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="aa58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa58a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa58a-103">CosmosDB Sql Trigger를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="aa58a-104">기존 트리거를 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="aa58a-105">구문</span><span class="sxs-lookup"><span data-stu-id="aa58a-105">SYNTAX</span></span>

### <span data-ttu-id="aa58a-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa58a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa58a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa58a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa58a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa58a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa58a-109">설명</span><span class="sxs-lookup"><span data-stu-id="aa58a-109">DESCRIPTION</span></span>
<span data-ttu-id="aa58a-110">CosmosDB Sql Trigger를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="aa58a-111">기존 트리거를 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="aa58a-112">예제</span><span class="sxs-lookup"><span data-stu-id="aa58a-112">EXAMPLES</span></span>

### <span data-ttu-id="aa58a-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa58a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="aa58a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa58a-114">PARAMETERS</span></span>

### <span data-ttu-id="aa58a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa58a-115">-AccountName</span></span>
<span data-ttu-id="aa58a-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aa58a-117">-Body</span><span class="sxs-lookup"><span data-stu-id="aa58a-117">-Body</span></span>
<span data-ttu-id="aa58a-118">트리거의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="aa58a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="aa58a-119">-Confirm</span></span>
<span data-ttu-id="aa58a-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa58a-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="aa58a-121">-ContainerName</span></span>
<span data-ttu-id="aa58a-122">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-122">Container name.</span></span>

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

### <span data-ttu-id="aa58a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa58a-123">-DatabaseName</span></span>
<span data-ttu-id="aa58a-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-124">Database name.</span></span>

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

### <span data-ttu-id="aa58a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa58a-125">-DefaultProfile</span></span>
<span data-ttu-id="aa58a-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa58a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa58a-127">-InputObject</span></span>
<span data-ttu-id="aa58a-128">Sql 트리거 개체</span><span class="sxs-lookup"><span data-stu-id="aa58a-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="aa58a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="aa58a-129">-Name</span></span>
<span data-ttu-id="aa58a-130">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-130">Trigger name.</span></span>

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

### <span data-ttu-id="aa58a-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aa58a-131">-ParentObject</span></span>
<span data-ttu-id="aa58a-132">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-132">Sql Container object.</span></span>

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

### <span data-ttu-id="aa58a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa58a-133">-ResourceGroupName</span></span>
<span data-ttu-id="aa58a-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-134">Name of resource group.</span></span>

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

### <span data-ttu-id="aa58a-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="aa58a-135">-TriggerOperation</span></span>
<span data-ttu-id="aa58a-136">트리거가 연결된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="aa58a-137">가능한 값은 다음과 같습니다. 'All', 'Create', 'Update', 'Delete', 'replace'</span><span class="sxs-lookup"><span data-stu-id="aa58a-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="aa58a-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="aa58a-138">-TriggerType</span></span>
<span data-ttu-id="aa58a-139">트리거의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-139">Type of the Trigger.</span></span>
<span data-ttu-id="aa58a-140">가능한 값은 다음과 같습니다. 'Pre', 'Post'</span><span class="sxs-lookup"><span data-stu-id="aa58a-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="aa58a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa58a-141">-WhatIf</span></span>
<span data-ttu-id="aa58a-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa58a-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa58a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa58a-144">CommonParameters</span></span>
<span data-ttu-id="aa58a-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa58a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa58a-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa58a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa58a-147">입력</span><span class="sxs-lookup"><span data-stu-id="aa58a-147">INPUTS</span></span>

### <span data-ttu-id="aa58a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="aa58a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="aa58a-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="aa58a-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="aa58a-150">출력</span><span class="sxs-lookup"><span data-stu-id="aa58a-150">OUTPUTS</span></span>

### <span data-ttu-id="aa58a-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="aa58a-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="aa58a-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="aa58a-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="aa58a-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa58a-153">NOTES</span></span>

## <span data-ttu-id="aa58a-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa58a-154">RELATED LINKS</span></span>
