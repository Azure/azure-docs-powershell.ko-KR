---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307259"
---
# <span data-ttu-id="e692b-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e692b-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e692b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e692b-102">SYNOPSIS</span></span>
<span data-ttu-id="e692b-103">CosmosDB Sql 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e692b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e692b-104">SYNTAX</span></span>

### <span data-ttu-id="e692b-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e692b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="e692b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e692b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e692b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e692b-107">DESCRIPTION</span></span>
<span data-ttu-id="e692b-108">**AzCosmosDBSqlContainer** cmdlet은 지정 된 ResourceGroupName, Accountname 및 databasename에 대 한 모든 기존 CosmosDB sql 컨테이너의 목록을 가져오고 지정 된 ResourceGroupName, Accountname, Databasename 및 ContainerName에 대 한 단일 CosmosDB sql 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="e692b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e692b-109">EXAMPLES</span></span>

### <span data-ttu-id="e692b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e692b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="e692b-111">변수</span><span class="sxs-lookup"><span data-stu-id="e692b-111">PARAMETERS</span></span>

### <span data-ttu-id="e692b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e692b-112">-AccountName</span></span>
<span data-ttu-id="e692b-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e692b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e692b-114">-DatabaseName</span></span>
<span data-ttu-id="e692b-115">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-115">Database name.</span></span>

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

### <span data-ttu-id="e692b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e692b-116">-DefaultProfile</span></span>
<span data-ttu-id="e692b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e692b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e692b-118">-Name</span></span>
<span data-ttu-id="e692b-119">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-119">Container name.</span></span>

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

### <span data-ttu-id="e692b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e692b-120">-ParentObject</span></span>
<span data-ttu-id="e692b-121">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="e692b-121">Sql Database object.</span></span>

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

### <span data-ttu-id="e692b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e692b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e692b-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-123">Name of resource group.</span></span>

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

### <span data-ttu-id="e692b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e692b-124">CommonParameters</span></span>
<span data-ttu-id="e692b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e692b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e692b-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e692b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e692b-127">입력</span><span class="sxs-lookup"><span data-stu-id="e692b-127">INPUTS</span></span>

### <span data-ttu-id="e692b-128">않아야</span><span class="sxs-lookup"><span data-stu-id="e692b-128">None</span></span>

## <span data-ttu-id="e692b-129">출력</span><span class="sxs-lookup"><span data-stu-id="e692b-129">OUTPUTS</span></span>

### <span data-ttu-id="e692b-130">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="e692b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e692b-131">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="e692b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e692b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e692b-132">NOTES</span></span>

## <span data-ttu-id="e692b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e692b-133">RELATED LINKS</span></span>
