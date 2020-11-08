---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034012"
---
# <span data-ttu-id="1a51b-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="1a51b-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="1a51b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a51b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a51b-103">기존 CosmosDB Sql 트리거를 새로 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="1a51b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a51b-104">SYNTAX</span></span>

### <span data-ttu-id="1a51b-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a51b-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a51b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a51b-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a51b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1a51b-107">DESCRIPTION</span></span>
<span data-ttu-id="1a51b-108">**AzCosmosDBSqlTrigger** cmdlet은 새 CosmosDB Sql 트리거를 새로 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="1a51b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1a51b-109">EXAMPLES</span></span>

### <span data-ttu-id="1a51b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a51b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="1a51b-111">변수</span><span class="sxs-lookup"><span data-stu-id="1a51b-111">PARAMETERS</span></span>

### <span data-ttu-id="1a51b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a51b-112">-AccountName</span></span>
<span data-ttu-id="1a51b-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1a51b-114">-본문</span><span class="sxs-lookup"><span data-stu-id="1a51b-114">-Body</span></span>
<span data-ttu-id="1a51b-115">트리거의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="1a51b-116">-확인</span><span class="sxs-lookup"><span data-stu-id="1a51b-116">-Confirm</span></span>
<span data-ttu-id="1a51b-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a51b-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1a51b-118">-ContainerName</span></span>
<span data-ttu-id="1a51b-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-119">Container name.</span></span>

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

### <span data-ttu-id="1a51b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a51b-120">-DatabaseName</span></span>
<span data-ttu-id="1a51b-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-121">Database name.</span></span>

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

### <span data-ttu-id="1a51b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a51b-122">-DefaultProfile</span></span>
<span data-ttu-id="1a51b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a51b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a51b-124">-InputObject</span></span>
<span data-ttu-id="1a51b-125">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="1a51b-125">Sql Container object.</span></span>

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

### <span data-ttu-id="1a51b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="1a51b-126">-Name</span></span>
<span data-ttu-id="1a51b-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-127">Trigger name.</span></span>

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

### <span data-ttu-id="1a51b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a51b-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a51b-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="1a51b-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="1a51b-130">-TriggerOperation</span></span>
<span data-ttu-id="1a51b-131">트리거가 연결 되는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="1a51b-132">사용할 수 있는 값은 다음과 같습니다. ' All ', ' Create ', ' Update ', ' Delete ', ' Replace '</span><span class="sxs-lookup"><span data-stu-id="1a51b-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="1a51b-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="1a51b-133">-TriggerType</span></span>
<span data-ttu-id="1a51b-134">트리거의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-134">Type of the Trigger.</span></span>
<span data-ttu-id="1a51b-135">사용할 수 있는 값은 다음과 같습니다. ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="1a51b-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="1a51b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a51b-136">-WhatIf</span></span>
<span data-ttu-id="1a51b-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a51b-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a51b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a51b-139">CommonParameters</span></span>
<span data-ttu-id="1a51b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a51b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a51b-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a51b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a51b-142">입력</span><span class="sxs-lookup"><span data-stu-id="1a51b-142">INPUTS</span></span>

### <span data-ttu-id="1a51b-143">않아야</span><span class="sxs-lookup"><span data-stu-id="1a51b-143">None</span></span>

## <span data-ttu-id="1a51b-144">출력</span><span class="sxs-lookup"><span data-stu-id="1a51b-144">OUTPUTS</span></span>

### <span data-ttu-id="1a51b-145">CosmosDB. PSSqlTriggerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="1a51b-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="1a51b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="1a51b-146">NOTES</span></span>

## <span data-ttu-id="1a51b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a51b-147">RELATED LINKS</span></span>
