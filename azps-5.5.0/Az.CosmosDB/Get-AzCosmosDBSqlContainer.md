---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204645"
---
# <span data-ttu-id="2d190-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2d190-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2d190-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d190-102">SYNOPSIS</span></span>
<span data-ttu-id="2d190-103">CosmosDB Sql 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2d190-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d190-104">SYNTAX</span></span>

### <span data-ttu-id="2d190-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2d190-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="2d190-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d190-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d190-107">설명</span><span class="sxs-lookup"><span data-stu-id="2d190-107">DESCRIPTION</span></span>
<span data-ttu-id="2d190-108">**Get-AzCosmosDBSqlContainer** cmdlet은 주어진 ResourceGroupName, AccountName 및 DatabaseName에 대한 모든 기존 CosmosDB Sql 컨테이너 목록을 구하고, 주어진 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 대한 단일 CosmosDB Sql 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="2d190-109">예제</span><span class="sxs-lookup"><span data-stu-id="2d190-109">EXAMPLES</span></span>

### <span data-ttu-id="2d190-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d190-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="2d190-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d190-111">PARAMETERS</span></span>

### <span data-ttu-id="2d190-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d190-112">-AccountName</span></span>
<span data-ttu-id="2d190-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2d190-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2d190-114">-DatabaseName</span></span>
<span data-ttu-id="2d190-115">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-115">Database name.</span></span>

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

### <span data-ttu-id="2d190-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d190-116">-DefaultProfile</span></span>
<span data-ttu-id="2d190-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d190-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2d190-118">-Name</span></span>
<span data-ttu-id="2d190-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-119">Container name.</span></span>

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

### <span data-ttu-id="2d190-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2d190-120">-ParentObject</span></span>
<span data-ttu-id="2d190-121">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d190-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d190-122">-ResourceGroupName</span></span>
<span data-ttu-id="2d190-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-123">Name of resource group.</span></span>

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

### <span data-ttu-id="2d190-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d190-124">CommonParameters</span></span>
<span data-ttu-id="2d190-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2d190-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d190-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2d190-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d190-127">입력</span><span class="sxs-lookup"><span data-stu-id="2d190-127">INPUTS</span></span>

### <span data-ttu-id="2d190-128">없음</span><span class="sxs-lookup"><span data-stu-id="2d190-128">None</span></span>

## <span data-ttu-id="2d190-129">출력</span><span class="sxs-lookup"><span data-stu-id="2d190-129">OUTPUTS</span></span>

### <span data-ttu-id="2d190-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2d190-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="2d190-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2d190-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2d190-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2d190-132">NOTES</span></span>

## <span data-ttu-id="2d190-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d190-133">RELATED LINKS</span></span>
