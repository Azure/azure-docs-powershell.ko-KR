---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333734"
---
# <span data-ttu-id="b35ad-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b35ad-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="b35ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b35ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b35ad-103">CosmosDB Sql Database를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b35ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="b35ad-104">SYNTAX</span></span>

### <span data-ttu-id="b35ad-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b35ad-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b35ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b35ad-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b35ad-107">설명</span><span class="sxs-lookup"><span data-stu-id="b35ad-107">DESCRIPTION</span></span>
<span data-ttu-id="b35ad-108">**Get-AzCosmosDBSqlDatabase** cmdlet은 주어진 ResourceGroupName, AccountName에 대한 모든 기존 CosmosDB Sql Database 목록을 구하고, 주어진 ResourceGroupName, AccountName, DatabaseName 및 ContainerName에 대한 단일 CosmosDB Sql Database를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="b35ad-109">예제</span><span class="sxs-lookup"><span data-stu-id="b35ad-109">EXAMPLES</span></span>

### <span data-ttu-id="b35ad-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b35ad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="b35ad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b35ad-111">PARAMETERS</span></span>

### <span data-ttu-id="b35ad-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b35ad-112">-AccountName</span></span>
<span data-ttu-id="b35ad-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b35ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35ad-114">-DefaultProfile</span></span>
<span data-ttu-id="b35ad-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35ad-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b35ad-116">-Name</span></span>
<span data-ttu-id="b35ad-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-117">Database name.</span></span>

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

### <span data-ttu-id="b35ad-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b35ad-118">-ParentObject</span></span>
<span data-ttu-id="b35ad-119">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="b35ad-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b35ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="b35ad-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-121">Name of resource group.</span></span>

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

### <span data-ttu-id="b35ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35ad-122">CommonParameters</span></span>
<span data-ttu-id="b35ad-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b35ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35ad-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b35ad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35ad-125">입력</span><span class="sxs-lookup"><span data-stu-id="b35ad-125">INPUTS</span></span>

### <span data-ttu-id="b35ad-126">없음</span><span class="sxs-lookup"><span data-stu-id="b35ad-126">None</span></span>

## <span data-ttu-id="b35ad-127">출력</span><span class="sxs-lookup"><span data-stu-id="b35ad-127">OUTPUTS</span></span>

### <span data-ttu-id="b35ad-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b35ad-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="b35ad-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b35ad-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b35ad-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b35ad-130">NOTES</span></span>

## <span data-ttu-id="b35ad-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b35ad-131">RELATED LINKS</span></span>
