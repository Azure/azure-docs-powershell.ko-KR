---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034023"
---
# <span data-ttu-id="859b1-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="859b1-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="859b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="859b1-102">SYNOPSIS</span></span>
<span data-ttu-id="859b1-103">CosmosDB Sql 저장 프로시저를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="859b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="859b1-104">SYNTAX</span></span>

### <span data-ttu-id="859b1-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="859b1-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="859b1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="859b1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="859b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="859b1-107">DESCRIPTION</span></span>
<span data-ttu-id="859b1-108">**AzCosmosDBSqlStoredProcedure** cmdlet은 지정 된 ResourceGroupName, Accountname, Databasename 및 ContainerName에 대 한 모든 기존 CosmosDB sql StoredProcedures 목록을 가져오고 지정 된 CosmosDB, Accountname, Databasename, Containername 및 ResourceGroupName에 대 한 단일 StoredProcedureName Sql 저장 프로시저를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="859b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="859b1-109">EXAMPLES</span></span>

### <span data-ttu-id="859b1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="859b1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="859b1-111">변수</span><span class="sxs-lookup"><span data-stu-id="859b1-111">PARAMETERS</span></span>

### <span data-ttu-id="859b1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="859b1-112">-AccountName</span></span>
<span data-ttu-id="859b1-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="859b1-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="859b1-114">-ContainerName</span></span>
<span data-ttu-id="859b1-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-115">Container name.</span></span>

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

### <span data-ttu-id="859b1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="859b1-116">-DatabaseName</span></span>
<span data-ttu-id="859b1-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-117">Database name.</span></span>

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

### <span data-ttu-id="859b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859b1-118">-DefaultProfile</span></span>
<span data-ttu-id="859b1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859b1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="859b1-120">-InputObject</span></span>
<span data-ttu-id="859b1-121">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="859b1-121">Sql Container object.</span></span>

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

### <span data-ttu-id="859b1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="859b1-122">-Name</span></span>
<span data-ttu-id="859b1-123">저장 된 Prcodecure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="859b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="859b1-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="859b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859b1-126">CommonParameters</span></span>
<span data-ttu-id="859b1-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="859b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859b1-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="859b1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859b1-129">입력</span><span class="sxs-lookup"><span data-stu-id="859b1-129">INPUTS</span></span>

### <span data-ttu-id="859b1-130">않아야</span><span class="sxs-lookup"><span data-stu-id="859b1-130">None</span></span>

## <span data-ttu-id="859b1-131">출력</span><span class="sxs-lookup"><span data-stu-id="859b1-131">OUTPUTS</span></span>

### <span data-ttu-id="859b1-132">CosmosDB. PSSqlStoredProcedureGetResults/.</span><span class="sxs-lookup"><span data-stu-id="859b1-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="859b1-133">상속자</span><span class="sxs-lookup"><span data-stu-id="859b1-133">NOTES</span></span>

## <span data-ttu-id="859b1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="859b1-134">RELATED LINKS</span></span>
