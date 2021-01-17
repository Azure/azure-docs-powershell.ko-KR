---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372919"
---
# <span data-ttu-id="7e0a0-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="7e0a0-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="7e0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0a0-103">CosmosDB Sql StoredProcedure를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="7e0a0-104">기존 StoredProcedure를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="7e0a0-105">구문</span><span class="sxs-lookup"><span data-stu-id="7e0a0-105">SYNTAX</span></span>

### <span data-ttu-id="7e0a0-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e0a0-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e0a0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e0a0-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e0a0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e0a0-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e0a0-109">설명</span><span class="sxs-lookup"><span data-stu-id="7e0a0-109">DESCRIPTION</span></span>
<span data-ttu-id="7e0a0-110">CosmosDB Sql StoredProcedure를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="7e0a0-111">기존 StoredProcedure를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="7e0a0-112">예제</span><span class="sxs-lookup"><span data-stu-id="7e0a0-112">EXAMPLES</span></span>

### <span data-ttu-id="7e0a0-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e0a0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="7e0a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e0a0-114">PARAMETERS</span></span>

### <span data-ttu-id="7e0a0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e0a0-115">-AccountName</span></span>
<span data-ttu-id="7e0a0-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7e0a0-117">-Body</span><span class="sxs-lookup"><span data-stu-id="7e0a0-117">-Body</span></span>
<span data-ttu-id="7e0a0-118">저장 프로시저의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="7e0a0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e0a0-119">-Confirm</span></span>
<span data-ttu-id="7e0a0-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e0a0-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7e0a0-121">-ContainerName</span></span>
<span data-ttu-id="7e0a0-122">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-122">Container name.</span></span>

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

### <span data-ttu-id="7e0a0-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e0a0-123">-DatabaseName</span></span>
<span data-ttu-id="7e0a0-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-124">Database name.</span></span>

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

### <span data-ttu-id="7e0a0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0a0-125">-DefaultProfile</span></span>
<span data-ttu-id="7e0a0-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0a0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e0a0-127">-InputObject</span></span>
<span data-ttu-id="7e0a0-128">Sql 저장 프로시저 개체</span><span class="sxs-lookup"><span data-stu-id="7e0a0-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0a0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7e0a0-129">-Name</span></span>
<span data-ttu-id="7e0a0-130">저장된 Prcodecure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="7e0a0-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7e0a0-131">-ParentObject</span></span>
<span data-ttu-id="7e0a0-132">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-132">Sql Container object.</span></span>

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

### <span data-ttu-id="7e0a0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0a0-133">-ResourceGroupName</span></span>
<span data-ttu-id="7e0a0-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-134">Name of resource group.</span></span>

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

### <span data-ttu-id="7e0a0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e0a0-135">-WhatIf</span></span>
<span data-ttu-id="7e0a0-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e0a0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e0a0-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e0a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0a0-138">CommonParameters</span></span>
<span data-ttu-id="7e0a0-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0a0-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e0a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0a0-141">입력</span><span class="sxs-lookup"><span data-stu-id="7e0a0-141">INPUTS</span></span>

### <span data-ttu-id="7e0a0-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7e0a0-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="7e0a0-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="7e0a0-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="7e0a0-144">출력</span><span class="sxs-lookup"><span data-stu-id="7e0a0-144">OUTPUTS</span></span>

### <span data-ttu-id="7e0a0-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="7e0a0-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="7e0a0-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7e0a0-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7e0a0-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e0a0-147">NOTES</span></span>

## <span data-ttu-id="7e0a0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e0a0-148">RELATED LINKS</span></span>
