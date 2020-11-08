---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212364"
---
# <span data-ttu-id="56237-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="56237-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="56237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56237-102">SYNOPSIS</span></span>
<span data-ttu-id="56237-103">CosmosDB Sql 저장 프로시저를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="56237-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="56237-104">기존 저장 프로시저를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="56237-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="56237-105">구문과</span><span class="sxs-lookup"><span data-stu-id="56237-105">SYNTAX</span></span>

### <span data-ttu-id="56237-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="56237-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56237-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56237-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56237-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56237-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56237-109">설명은</span><span class="sxs-lookup"><span data-stu-id="56237-109">DESCRIPTION</span></span>
<span data-ttu-id="56237-110">CosmosDB Sql 저장 프로시저를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="56237-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="56237-111">기존 저장 프로시저를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="56237-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="56237-112">예제의</span><span class="sxs-lookup"><span data-stu-id="56237-112">EXAMPLES</span></span>

### <span data-ttu-id="56237-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="56237-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="56237-114">변수</span><span class="sxs-lookup"><span data-stu-id="56237-114">PARAMETERS</span></span>

### <span data-ttu-id="56237-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56237-115">-AccountName</span></span>
<span data-ttu-id="56237-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="56237-117">-본문</span><span class="sxs-lookup"><span data-stu-id="56237-117">-Body</span></span>
<span data-ttu-id="56237-118">저장 프로시저의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="56237-119">-확인</span><span class="sxs-lookup"><span data-stu-id="56237-119">-Confirm</span></span>
<span data-ttu-id="56237-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56237-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56237-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="56237-121">-ContainerName</span></span>
<span data-ttu-id="56237-122">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-122">Container name.</span></span>

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

### <span data-ttu-id="56237-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56237-123">-DatabaseName</span></span>
<span data-ttu-id="56237-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-124">Database name.</span></span>

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

### <span data-ttu-id="56237-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56237-125">-DefaultProfile</span></span>
<span data-ttu-id="56237-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56237-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56237-127">-InputObject</span></span>
<span data-ttu-id="56237-128">Sql 저장 프로시저 개체</span><span class="sxs-lookup"><span data-stu-id="56237-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="56237-129">-이름</span><span class="sxs-lookup"><span data-stu-id="56237-129">-Name</span></span>
<span data-ttu-id="56237-130">저장 된 Prcodecure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="56237-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="56237-131">-ParentObject</span></span>
<span data-ttu-id="56237-132">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="56237-132">Sql Container object.</span></span>

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

### <span data-ttu-id="56237-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56237-133">-ResourceGroupName</span></span>
<span data-ttu-id="56237-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56237-134">Name of resource group.</span></span>

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

### <span data-ttu-id="56237-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56237-135">-WhatIf</span></span>
<span data-ttu-id="56237-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56237-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56237-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56237-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56237-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56237-138">CommonParameters</span></span>
<span data-ttu-id="56237-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56237-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56237-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56237-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56237-141">입력</span><span class="sxs-lookup"><span data-stu-id="56237-141">INPUTS</span></span>

### <span data-ttu-id="56237-142">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="56237-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="56237-143">CosmosDB. PSSqlStoredProcedureGetResults/.</span><span class="sxs-lookup"><span data-stu-id="56237-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="56237-144">출력</span><span class="sxs-lookup"><span data-stu-id="56237-144">OUTPUTS</span></span>

### <span data-ttu-id="56237-145">CosmosDB. PSSqlStoredProcedureGetResults/.</span><span class="sxs-lookup"><span data-stu-id="56237-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="56237-146">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="56237-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="56237-147">상속자</span><span class="sxs-lookup"><span data-stu-id="56237-147">NOTES</span></span>

## <span data-ttu-id="56237-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56237-148">RELATED LINKS</span></span>
