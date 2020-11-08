---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044108"
---
# <span data-ttu-id="ac7f4-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="ac7f4-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="ac7f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7f4-103">CosmosDB Sql 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="ac7f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac7f4-104">SYNTAX</span></span>

### <span data-ttu-id="ac7f4-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ac7f4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="ac7f4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac7f4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac7f4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ac7f4-107">DESCRIPTION</span></span>
<span data-ttu-id="ac7f4-108">**AzCosmosDBSqlContainer** cmdlet은 지정 된 ResourceGroupName, Accountname 및 databasename에 대 한 모든 기존 CosmosDB sql 컨테이너의 목록을 가져오고 지정 된 ResourceGroupName, Accountname, Databasename 및 ContainerName에 대 한 단일 CosmosDB sql 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="ac7f4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ac7f4-109">EXAMPLES</span></span>

### <span data-ttu-id="ac7f4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac7f4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="ac7f4-111">변수</span><span class="sxs-lookup"><span data-stu-id="ac7f4-111">PARAMETERS</span></span>

### <span data-ttu-id="ac7f4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ac7f4-112">-AccountName</span></span>
<span data-ttu-id="ac7f4-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ac7f4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ac7f4-114">-DatabaseName</span></span>
<span data-ttu-id="ac7f4-115">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-115">Database name.</span></span>

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

### <span data-ttu-id="ac7f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac7f4-116">-DefaultProfile</span></span>
<span data-ttu-id="ac7f4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac7f4-118">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="ac7f4-118">-Detailed</span></span>
<span data-ttu-id="ac7f4-119">그런 다음 cmdlet은 처리 값이 포함 된 컨테이너를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac7f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac7f4-120">-InputObject</span></span>
<span data-ttu-id="ac7f4-121">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-121">Sql Database object.</span></span>

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

### <span data-ttu-id="ac7f4-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ac7f4-122">-Name</span></span>
<span data-ttu-id="ac7f4-123">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-123">Container name.</span></span>

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

### <span data-ttu-id="ac7f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac7f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac7f4-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-125">Name of resource group.</span></span>

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

### <span data-ttu-id="ac7f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7f4-126">CommonParameters</span></span>
<span data-ttu-id="ac7f4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7f4-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7f4-129">입력</span><span class="sxs-lookup"><span data-stu-id="ac7f4-129">INPUTS</span></span>

### <span data-ttu-id="ac7f4-130">않아야</span><span class="sxs-lookup"><span data-stu-id="ac7f4-130">None</span></span>

## <span data-ttu-id="ac7f4-131">출력</span><span class="sxs-lookup"><span data-stu-id="ac7f4-131">OUTPUTS</span></span>

### <span data-ttu-id="ac7f4-132">CosmosDB. PSSqlContainerGetResults/.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="ac7f4-133">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="ac7f4-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ac7f4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ac7f4-134">NOTES</span></span>

## <span data-ttu-id="ac7f4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac7f4-135">RELATED LINKS</span></span>
