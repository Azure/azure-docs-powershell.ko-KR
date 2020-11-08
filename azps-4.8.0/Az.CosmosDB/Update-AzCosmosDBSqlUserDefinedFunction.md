---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214186"
---
# <span data-ttu-id="c35a0-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="c35a0-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="c35a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c35a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c35a0-103">CosmosDB Sql UserDefinedFunction를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="c35a0-104">기존 UserDefinedFunction를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="c35a0-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c35a0-105">SYNTAX</span></span>

### <span data-ttu-id="c35a0-106">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c35a0-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c35a0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c35a0-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c35a0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c35a0-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c35a0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c35a0-109">DESCRIPTION</span></span>
<span data-ttu-id="c35a0-110">CosmosDB Sql UserDefinedFunction를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="c35a0-111">기존 UserDefinedFunction를 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="c35a0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c35a0-112">EXAMPLES</span></span>

### <span data-ttu-id="c35a0-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c35a0-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="c35a0-114">변수</span><span class="sxs-lookup"><span data-stu-id="c35a0-114">PARAMETERS</span></span>

### <span data-ttu-id="c35a0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c35a0-115">-AccountName</span></span>
<span data-ttu-id="c35a0-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c35a0-117">-본문</span><span class="sxs-lookup"><span data-stu-id="c35a0-117">-Body</span></span>
<span data-ttu-id="c35a0-118">사용자 정의 함수의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="c35a0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c35a0-119">-Confirm</span></span>
<span data-ttu-id="c35a0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c35a0-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c35a0-121">-ContainerName</span></span>
<span data-ttu-id="c35a0-122">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-122">Container name.</span></span>

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

### <span data-ttu-id="c35a0-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c35a0-123">-DatabaseName</span></span>
<span data-ttu-id="c35a0-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-124">Database name.</span></span>

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

### <span data-ttu-id="c35a0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35a0-125">-DefaultProfile</span></span>
<span data-ttu-id="c35a0-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c35a0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c35a0-127">-InputObject</span></span>
<span data-ttu-id="c35a0-128">Sql 사용자 정의 함수 개체</span><span class="sxs-lookup"><span data-stu-id="c35a0-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c35a0-129">-이름</span><span class="sxs-lookup"><span data-stu-id="c35a0-129">-Name</span></span>
<span data-ttu-id="c35a0-130">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="c35a0-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c35a0-131">-ParentObject</span></span>
<span data-ttu-id="c35a0-132">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="c35a0-132">Sql Container object.</span></span>

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

### <span data-ttu-id="c35a0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35a0-133">-ResourceGroupName</span></span>
<span data-ttu-id="c35a0-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-134">Name of resource group.</span></span>

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

### <span data-ttu-id="c35a0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c35a0-135">-WhatIf</span></span>
<span data-ttu-id="c35a0-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c35a0-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c35a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35a0-138">CommonParameters</span></span>
<span data-ttu-id="c35a0-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35a0-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c35a0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35a0-141">입력</span><span class="sxs-lookup"><span data-stu-id="c35a0-141">INPUTS</span></span>

### <span data-ttu-id="c35a0-142">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c35a0-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="c35a0-143">CosmosDB. PSSqlUserDefinedFunctionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c35a0-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="c35a0-144">출력</span><span class="sxs-lookup"><span data-stu-id="c35a0-144">OUTPUTS</span></span>

### <span data-ttu-id="c35a0-145">CosmosDB. PSSqlUserDefinedFunctionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c35a0-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="c35a0-146">CosmosDB (ResourceNotFoundException).</span><span class="sxs-lookup"><span data-stu-id="c35a0-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c35a0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c35a0-147">NOTES</span></span>

## <span data-ttu-id="c35a0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c35a0-148">RELATED LINKS</span></span>
