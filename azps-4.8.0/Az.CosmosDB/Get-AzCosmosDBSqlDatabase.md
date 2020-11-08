---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214198"
---
# <span data-ttu-id="077cd-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="077cd-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="077cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="077cd-102">SYNOPSIS</span></span>
<span data-ttu-id="077cd-103">CosmosDB Sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="077cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="077cd-104">SYNTAX</span></span>

### <span data-ttu-id="077cd-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="077cd-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="077cd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="077cd-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="077cd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="077cd-107">DESCRIPTION</span></span>
<span data-ttu-id="077cd-108">**AzCosmosDBSqlDatabase** cmdlet은 지정 된 ResourceGroupName 및 accountname에 대 한 모든 기존 CosmosDB sql 데이터베이스 목록을 가져오고 지정 된 ResourceGroupName, Accountname, DatabaseName 및 ContainerName에 대 한 단일 CosmosDB sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="077cd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="077cd-109">EXAMPLES</span></span>

### <span data-ttu-id="077cd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="077cd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="077cd-111">변수</span><span class="sxs-lookup"><span data-stu-id="077cd-111">PARAMETERS</span></span>

### <span data-ttu-id="077cd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="077cd-112">-AccountName</span></span>
<span data-ttu-id="077cd-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="077cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077cd-114">-DefaultProfile</span></span>
<span data-ttu-id="077cd-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="077cd-116">-이름</span><span class="sxs-lookup"><span data-stu-id="077cd-116">-Name</span></span>
<span data-ttu-id="077cd-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-117">Database name.</span></span>

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

### <span data-ttu-id="077cd-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="077cd-118">-ParentObject</span></span>
<span data-ttu-id="077cd-119">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="077cd-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="077cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="077cd-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-121">Name of resource group.</span></span>

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

### <span data-ttu-id="077cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077cd-122">CommonParameters</span></span>
<span data-ttu-id="077cd-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="077cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077cd-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="077cd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077cd-125">입력</span><span class="sxs-lookup"><span data-stu-id="077cd-125">INPUTS</span></span>

### <span data-ttu-id="077cd-126">않아야</span><span class="sxs-lookup"><span data-stu-id="077cd-126">None</span></span>

## <span data-ttu-id="077cd-127">출력</span><span class="sxs-lookup"><span data-stu-id="077cd-127">OUTPUTS</span></span>

### <span data-ttu-id="077cd-128">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="077cd-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="077cd-129">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="077cd-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="077cd-130">상속자</span><span class="sxs-lookup"><span data-stu-id="077cd-130">NOTES</span></span>

## <span data-ttu-id="077cd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="077cd-131">RELATED LINKS</span></span>
