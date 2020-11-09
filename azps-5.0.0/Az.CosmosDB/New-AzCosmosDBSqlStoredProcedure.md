---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306974"
---
# <span data-ttu-id="aec66-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="aec66-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="aec66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec66-102">SYNOPSIS</span></span>
<span data-ttu-id="aec66-103">새 CosmosDB Sql 저장 프로시저를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="aec66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aec66-104">SYNTAX</span></span>

### <span data-ttu-id="aec66-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aec66-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec66-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aec66-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec66-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aec66-107">DESCRIPTION</span></span>
<span data-ttu-id="aec66-108">새 CosmosDB Sql 저장 프로시저를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="aec66-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aec66-109">EXAMPLES</span></span>

### <span data-ttu-id="aec66-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="aec66-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="aec66-111">변수</span><span class="sxs-lookup"><span data-stu-id="aec66-111">PARAMETERS</span></span>

### <span data-ttu-id="aec66-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aec66-112">-AccountName</span></span>
<span data-ttu-id="aec66-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aec66-114">-본문</span><span class="sxs-lookup"><span data-stu-id="aec66-114">-Body</span></span>
<span data-ttu-id="aec66-115">저장 프로시저의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="aec66-116">-확인</span><span class="sxs-lookup"><span data-stu-id="aec66-116">-Confirm</span></span>
<span data-ttu-id="aec66-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec66-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="aec66-118">-ContainerName</span></span>
<span data-ttu-id="aec66-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-119">Container name.</span></span>

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

### <span data-ttu-id="aec66-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aec66-120">-DatabaseName</span></span>
<span data-ttu-id="aec66-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-121">Database name.</span></span>

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

### <span data-ttu-id="aec66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec66-122">-DefaultProfile</span></span>
<span data-ttu-id="aec66-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec66-124">-이름</span><span class="sxs-lookup"><span data-stu-id="aec66-124">-Name</span></span>
<span data-ttu-id="aec66-125">저장 된 Prcodecure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="aec66-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="aec66-126">-ParentObject</span></span>
<span data-ttu-id="aec66-127">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="aec66-127">Sql Container object.</span></span>

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

### <span data-ttu-id="aec66-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec66-128">-ResourceGroupName</span></span>
<span data-ttu-id="aec66-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-129">Name of resource group.</span></span>

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

### <span data-ttu-id="aec66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec66-130">-WhatIf</span></span>
<span data-ttu-id="aec66-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec66-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec66-133">CommonParameters</span></span>
<span data-ttu-id="aec66-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aec66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec66-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aec66-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec66-136">입력</span><span class="sxs-lookup"><span data-stu-id="aec66-136">INPUTS</span></span>

### <span data-ttu-id="aec66-137">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="aec66-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="aec66-138">출력</span><span class="sxs-lookup"><span data-stu-id="aec66-138">OUTPUTS</span></span>

### <span data-ttu-id="aec66-139">CosmosDB. PSSqlStoredProcedureGetResults/.</span><span class="sxs-lookup"><span data-stu-id="aec66-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="aec66-140">CosmosDB (ConflictingResourceException).</span><span class="sxs-lookup"><span data-stu-id="aec66-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="aec66-141">상속자</span><span class="sxs-lookup"><span data-stu-id="aec66-141">NOTES</span></span>

## <span data-ttu-id="aec66-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aec66-142">RELATED LINKS</span></span>
