---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0d422014d3cf2ca2ffa18b60c10b50b21bf91144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986902"
---
# <span data-ttu-id="48c0d-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="48c0d-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="48c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="48c0d-103">CosmosDB Sql User Defined 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="48c0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="48c0d-104">SYNTAX</span></span>

### <span data-ttu-id="48c0d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c0d-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48c0d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48c0d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48c0d-107">설명</span><span class="sxs-lookup"><span data-stu-id="48c0d-107">DESCRIPTION</span></span>
<span data-ttu-id="48c0d-108">**Get-AzCosmosDBSqlUserDefinedFunction** cmdlet은 주어진 ResourceGroupName에 대한 모든 기존 CosmosDB Sql UserDefinedFunctions 목록을 얻습니다. AccountName, DatabaseName 및 ContainerName 및 주어진 ResourceGroupName, AccountName, DatabaseName, ContainerName 및 UserDefinedFunctionName에 대한 단일 CosmosDB Sql UserDefinedFunction을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="48c0d-109">예제</span><span class="sxs-lookup"><span data-stu-id="48c0d-109">EXAMPLES</span></span>

### <span data-ttu-id="48c0d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="48c0d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="48c0d-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48c0d-111">PARAMETERS</span></span>

### <span data-ttu-id="48c0d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48c0d-112">-AccountName</span></span>
<span data-ttu-id="48c0d-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="48c0d-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="48c0d-114">-ContainerName</span></span>
<span data-ttu-id="48c0d-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-115">Container name.</span></span>

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

### <span data-ttu-id="48c0d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48c0d-116">-DatabaseName</span></span>
<span data-ttu-id="48c0d-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-117">Database name.</span></span>

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

### <span data-ttu-id="48c0d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c0d-118">-DefaultProfile</span></span>
<span data-ttu-id="48c0d-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c0d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="48c0d-120">-Name</span></span>
<span data-ttu-id="48c0d-121">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="48c0d-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="48c0d-122">-ParentObject</span></span>
<span data-ttu-id="48c0d-123">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-123">Sql Container object.</span></span>

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

### <span data-ttu-id="48c0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="48c0d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-125">Name of resource group.</span></span>

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

### <span data-ttu-id="48c0d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c0d-126">CommonParameters</span></span>
<span data-ttu-id="48c0d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48c0d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c0d-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48c0d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c0d-129">입력</span><span class="sxs-lookup"><span data-stu-id="48c0d-129">INPUTS</span></span>

### <span data-ttu-id="48c0d-130">없음</span><span class="sxs-lookup"><span data-stu-id="48c0d-130">None</span></span>

## <span data-ttu-id="48c0d-131">출력</span><span class="sxs-lookup"><span data-stu-id="48c0d-131">OUTPUTS</span></span>

### <span data-ttu-id="48c0d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="48c0d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="48c0d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48c0d-133">NOTES</span></span>

## <span data-ttu-id="48c0d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48c0d-134">RELATED LINKS</span></span>
