---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879569"
---
# <span data-ttu-id="35d50-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="35d50-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="35d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35d50-102">SYNOPSIS</span></span>
<span data-ttu-id="35d50-103">CosmosDB Sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="35d50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35d50-104">SYNTAX</span></span>

### <span data-ttu-id="35d50-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="35d50-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35d50-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35d50-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35d50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35d50-107">DESCRIPTION</span></span>
<span data-ttu-id="35d50-108">**AzCosmosDBSqlDatabase** cmdlet은 지정 된 ResourceGroupName 및 accountname에 대 한 모든 기존 CosmosDB sql 데이터베이스 목록을 가져오고 지정 된 ResourceGroupName, Accountname, DatabaseName 및 ContainerName에 대 한 단일 CosmosDB sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="35d50-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35d50-109">EXAMPLES</span></span>

### <span data-ttu-id="35d50-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="35d50-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="35d50-111">변수</span><span class="sxs-lookup"><span data-stu-id="35d50-111">PARAMETERS</span></span>

### <span data-ttu-id="35d50-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="35d50-112">-AccountName</span></span>
<span data-ttu-id="35d50-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="35d50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d50-114">-DefaultProfile</span></span>
<span data-ttu-id="35d50-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d50-116">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="35d50-116">-Detailed</span></span>
<span data-ttu-id="35d50-117">그런 다음 cmdlet은 처리 값이 포함 된 컨테이너를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="35d50-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35d50-118">-InputObject</span></span>
<span data-ttu-id="35d50-119">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="35d50-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d50-120">-이름</span><span class="sxs-lookup"><span data-stu-id="35d50-120">-Name</span></span>
<span data-ttu-id="35d50-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-121">Database name.</span></span>

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

### <span data-ttu-id="35d50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d50-122">-ResourceGroupName</span></span>
<span data-ttu-id="35d50-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-123">Name of resource group.</span></span>

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

### <span data-ttu-id="35d50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d50-124">CommonParameters</span></span>
<span data-ttu-id="35d50-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35d50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d50-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35d50-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d50-127">입력</span><span class="sxs-lookup"><span data-stu-id="35d50-127">INPUTS</span></span>

### <span data-ttu-id="35d50-128">않아야</span><span class="sxs-lookup"><span data-stu-id="35d50-128">None</span></span>

## <span data-ttu-id="35d50-129">출력</span><span class="sxs-lookup"><span data-stu-id="35d50-129">OUTPUTS</span></span>

### <span data-ttu-id="35d50-130">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="35d50-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="35d50-131">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="35d50-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="35d50-132">상속자</span><span class="sxs-lookup"><span data-stu-id="35d50-132">NOTES</span></span>

## <span data-ttu-id="35d50-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35d50-133">RELATED LINKS</span></span>
