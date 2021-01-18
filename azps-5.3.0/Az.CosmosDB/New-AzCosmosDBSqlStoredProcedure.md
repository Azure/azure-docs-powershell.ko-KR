---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493681"
---
# <span data-ttu-id="dcad3-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="dcad3-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="dcad3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcad3-102">SYNOPSIS</span></span>
<span data-ttu-id="dcad3-103">새 CosmosDB Sql StoredProcedure를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="dcad3-104">구문</span><span class="sxs-lookup"><span data-stu-id="dcad3-104">SYNTAX</span></span>

### <span data-ttu-id="dcad3-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dcad3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcad3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcad3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcad3-107">설명</span><span class="sxs-lookup"><span data-stu-id="dcad3-107">DESCRIPTION</span></span>
<span data-ttu-id="dcad3-108">새 CosmosDB Sql StoredProcedure를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="dcad3-109">예제</span><span class="sxs-lookup"><span data-stu-id="dcad3-109">EXAMPLES</span></span>

### <span data-ttu-id="dcad3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dcad3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="dcad3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcad3-111">PARAMETERS</span></span>

### <span data-ttu-id="dcad3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dcad3-112">-AccountName</span></span>
<span data-ttu-id="dcad3-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dcad3-114">-Body</span><span class="sxs-lookup"><span data-stu-id="dcad3-114">-Body</span></span>
<span data-ttu-id="dcad3-115">저장 프로시저의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="dcad3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcad3-116">-Confirm</span></span>
<span data-ttu-id="dcad3-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcad3-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dcad3-118">-ContainerName</span></span>
<span data-ttu-id="dcad3-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-119">Container name.</span></span>

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

### <span data-ttu-id="dcad3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dcad3-120">-DatabaseName</span></span>
<span data-ttu-id="dcad3-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-121">Database name.</span></span>

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

### <span data-ttu-id="dcad3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcad3-122">-DefaultProfile</span></span>
<span data-ttu-id="dcad3-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcad3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dcad3-124">-Name</span></span>
<span data-ttu-id="dcad3-125">저장된 Prcodecure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="dcad3-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dcad3-126">-ParentObject</span></span>
<span data-ttu-id="dcad3-127">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-127">Sql Container object.</span></span>

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

### <span data-ttu-id="dcad3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcad3-128">-ResourceGroupName</span></span>
<span data-ttu-id="dcad3-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-129">Name of resource group.</span></span>

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

### <span data-ttu-id="dcad3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcad3-130">-WhatIf</span></span>
<span data-ttu-id="dcad3-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dcad3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcad3-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcad3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcad3-133">CommonParameters</span></span>
<span data-ttu-id="dcad3-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dcad3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcad3-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dcad3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcad3-136">입력</span><span class="sxs-lookup"><span data-stu-id="dcad3-136">INPUTS</span></span>

### <span data-ttu-id="dcad3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="dcad3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="dcad3-138">출력</span><span class="sxs-lookup"><span data-stu-id="dcad3-138">OUTPUTS</span></span>

### <span data-ttu-id="dcad3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="dcad3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="dcad3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="dcad3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="dcad3-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dcad3-141">NOTES</span></span>

## <span data-ttu-id="dcad3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcad3-142">RELATED LINKS</span></span>
