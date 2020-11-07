---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: c8cfb1077f418c9d671729cb0ff762141a7b77c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877854"
---
# <span data-ttu-id="e7f72-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="e7f72-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="e7f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f72-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f72-103">CosmosDB Sql 사용자 정의 함수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="e7f72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7f72-104">SYNTAX</span></span>

### <span data-ttu-id="e7f72-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7f72-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7f72-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7f72-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7f72-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7f72-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f72-108">**AzCosmosDBSqlUserDefinedFunction** cmdlet은 지정 된 ResourceGroupName, Accountname, Databasename 및 ContainerName에 대 한 모든 기존 CosmosDB sql UserDefinedFunctions 목록을 가져오고 지정 된 CosmosDB, Accountname, Databasename, Containername 및 UserDefinedFunction에 대 한 단일 ResourceGroupName sql UserDefinedFunctionName를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="e7f72-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7f72-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f72-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7f72-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="e7f72-111">변수</span><span class="sxs-lookup"><span data-stu-id="e7f72-111">PARAMETERS</span></span>

### <span data-ttu-id="e7f72-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7f72-112">-AccountName</span></span>
<span data-ttu-id="e7f72-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7f72-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e7f72-114">-ContainerName</span></span>
<span data-ttu-id="e7f72-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-115">Container name.</span></span>

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

### <span data-ttu-id="e7f72-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7f72-116">-DatabaseName</span></span>
<span data-ttu-id="e7f72-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-117">Database name.</span></span>

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

### <span data-ttu-id="e7f72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f72-118">-DefaultProfile</span></span>
<span data-ttu-id="e7f72-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f72-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f72-120">-InputObject</span></span>
<span data-ttu-id="e7f72-121">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="e7f72-121">Sql Container object.</span></span>

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

### <span data-ttu-id="e7f72-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e7f72-122">-Name</span></span>
<span data-ttu-id="e7f72-123">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-123">User Defined Function Name.</span></span>

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

### <span data-ttu-id="e7f72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f72-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7f72-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-125">Name of resource group.</span></span>

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

### <span data-ttu-id="e7f72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f72-126">CommonParameters</span></span>
<span data-ttu-id="e7f72-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f72-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f72-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f72-129">입력</span><span class="sxs-lookup"><span data-stu-id="e7f72-129">INPUTS</span></span>

### <span data-ttu-id="e7f72-130">않아야</span><span class="sxs-lookup"><span data-stu-id="e7f72-130">None</span></span>

## <span data-ttu-id="e7f72-131">출력</span><span class="sxs-lookup"><span data-stu-id="e7f72-131">OUTPUTS</span></span>

### <span data-ttu-id="e7f72-132">CosmosDB. PSSqlUserDefinedFunctionGetResults/.</span><span class="sxs-lookup"><span data-stu-id="e7f72-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="e7f72-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e7f72-133">NOTES</span></span>

## <span data-ttu-id="e7f72-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7f72-134">RELATED LINKS</span></span>
