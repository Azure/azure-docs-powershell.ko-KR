---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0ad79ff742647395b48c8af3b41140b1a7bda691
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980843"
---
# <span data-ttu-id="7a83a-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="7a83a-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="7a83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a83a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a83a-103">새 CosmosDB Sql UserDefinedFunction을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="7a83a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a83a-104">SYNTAX</span></span>

### <span data-ttu-id="7a83a-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a83a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a83a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a83a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a83a-107">설명</span><span class="sxs-lookup"><span data-stu-id="7a83a-107">DESCRIPTION</span></span>
<span data-ttu-id="7a83a-108">새 CosmosDB Sql UserDefinedFunction을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="7a83a-109">예제</span><span class="sxs-lookup"><span data-stu-id="7a83a-109">EXAMPLES</span></span>

### <span data-ttu-id="7a83a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a83a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="7a83a-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a83a-111">PARAMETERS</span></span>

### <span data-ttu-id="7a83a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a83a-112">-AccountName</span></span>
<span data-ttu-id="7a83a-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7a83a-114">-Body</span><span class="sxs-lookup"><span data-stu-id="7a83a-114">-Body</span></span>
<span data-ttu-id="7a83a-115">사용자 정의 함수의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="7a83a-116">-확인</span><span class="sxs-lookup"><span data-stu-id="7a83a-116">-Confirm</span></span>
<span data-ttu-id="7a83a-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a83a-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7a83a-118">-ContainerName</span></span>
<span data-ttu-id="7a83a-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-119">Container name.</span></span>

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

### <span data-ttu-id="7a83a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a83a-120">-DatabaseName</span></span>
<span data-ttu-id="7a83a-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-121">Database name.</span></span>

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

### <span data-ttu-id="7a83a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a83a-122">-DefaultProfile</span></span>
<span data-ttu-id="7a83a-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a83a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7a83a-124">-Name</span></span>
<span data-ttu-id="7a83a-125">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="7a83a-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7a83a-126">-ParentObject</span></span>
<span data-ttu-id="7a83a-127">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-127">Sql Container object.</span></span>

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

### <span data-ttu-id="7a83a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a83a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7a83a-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="7a83a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a83a-130">-WhatIf</span></span>
<span data-ttu-id="7a83a-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a83a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a83a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a83a-133">CommonParameters</span></span>
<span data-ttu-id="7a83a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a83a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a83a-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a83a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a83a-136">입력</span><span class="sxs-lookup"><span data-stu-id="7a83a-136">INPUTS</span></span>

### <span data-ttu-id="7a83a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7a83a-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="7a83a-138">출력</span><span class="sxs-lookup"><span data-stu-id="7a83a-138">OUTPUTS</span></span>

### <span data-ttu-id="7a83a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="7a83a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="7a83a-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="7a83a-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="7a83a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a83a-141">NOTES</span></span>

## <span data-ttu-id="7a83a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a83a-142">RELATED LINKS</span></span>
