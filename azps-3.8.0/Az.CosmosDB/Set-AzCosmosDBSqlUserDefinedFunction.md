---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877377"
---
# <span data-ttu-id="88761-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="88761-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="88761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88761-102">SYNOPSIS</span></span>
<span data-ttu-id="88761-103">새 CosmosDB Sql UserDefinedFunction를 만들거나 기존에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="88761-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="88761-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88761-104">SYNTAX</span></span>

### <span data-ttu-id="88761-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="88761-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88761-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88761-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88761-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88761-107">DESCRIPTION</span></span>
<span data-ttu-id="88761-108">**AzCosmosDBSqlUserDefinedFunction** cmdlet은 새 CosmosDB Sql UserDefinedFunction을 만들거나 기존에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="88761-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="88761-109">예제의</span><span class="sxs-lookup"><span data-stu-id="88761-109">EXAMPLES</span></span>

### <span data-ttu-id="88761-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="88761-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="88761-111">변수</span><span class="sxs-lookup"><span data-stu-id="88761-111">PARAMETERS</span></span>

### <span data-ttu-id="88761-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="88761-112">-AccountName</span></span>
<span data-ttu-id="88761-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="88761-114">-본문</span><span class="sxs-lookup"><span data-stu-id="88761-114">-Body</span></span>
<span data-ttu-id="88761-115">사용자 정의 함수의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="88761-116">-확인</span><span class="sxs-lookup"><span data-stu-id="88761-116">-Confirm</span></span>
<span data-ttu-id="88761-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88761-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88761-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="88761-118">-ContainerName</span></span>
<span data-ttu-id="88761-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-119">Container name.</span></span>

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

### <span data-ttu-id="88761-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88761-120">-DatabaseName</span></span>
<span data-ttu-id="88761-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-121">Database name.</span></span>

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

### <span data-ttu-id="88761-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88761-122">-DefaultProfile</span></span>
<span data-ttu-id="88761-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88761-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88761-124">-InputObject</span></span>
<span data-ttu-id="88761-125">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="88761-125">Sql Container object.</span></span>

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

### <span data-ttu-id="88761-126">-이름</span><span class="sxs-lookup"><span data-stu-id="88761-126">-Name</span></span>
<span data-ttu-id="88761-127">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-127">User Defined Function Name.</span></span>

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

### <span data-ttu-id="88761-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88761-128">-ResourceGroupName</span></span>
<span data-ttu-id="88761-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88761-129">Name of resource group.</span></span>

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

### <span data-ttu-id="88761-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88761-130">-WhatIf</span></span>
<span data-ttu-id="88761-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88761-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88761-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88761-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88761-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88761-133">CommonParameters</span></span>
<span data-ttu-id="88761-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88761-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88761-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="88761-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88761-136">입력</span><span class="sxs-lookup"><span data-stu-id="88761-136">INPUTS</span></span>

### <span data-ttu-id="88761-137">않아야</span><span class="sxs-lookup"><span data-stu-id="88761-137">None</span></span>

## <span data-ttu-id="88761-138">출력</span><span class="sxs-lookup"><span data-stu-id="88761-138">OUTPUTS</span></span>

### <span data-ttu-id="88761-139">CosmosDB. PSSqlUserDefinedFunctionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="88761-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="88761-140">상속자</span><span class="sxs-lookup"><span data-stu-id="88761-140">NOTES</span></span>

## <span data-ttu-id="88761-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88761-141">RELATED LINKS</span></span>
