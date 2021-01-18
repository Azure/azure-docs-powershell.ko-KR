---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495821"
---
# <span data-ttu-id="162fb-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="162fb-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="162fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="162fb-102">SYNOPSIS</span></span>
<span data-ttu-id="162fb-103">CosmosDB Sql StoredProcedure를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="162fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="162fb-104">SYNTAX</span></span>

### <span data-ttu-id="162fb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="162fb-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="162fb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="162fb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="162fb-107">설명</span><span class="sxs-lookup"><span data-stu-id="162fb-107">DESCRIPTION</span></span>
<span data-ttu-id="162fb-108">**Get-AzCosmosDBSqlStoredProcedure** cmdlet은 주어진 ResourceGroupName에 대한 모든 기존 CosmosDB Sql StoredProcedures 목록을 얻습니다. AccountName, DatabaseName 및 ContainerName 및 주어진 ResourceGroupName, AccountName, DatabaseName, ContainerName 및 StoredProcedureName에 대한 단일 CosmosDB Sql StoredProcedure를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="162fb-109">예제</span><span class="sxs-lookup"><span data-stu-id="162fb-109">EXAMPLES</span></span>

### <span data-ttu-id="162fb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="162fb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="162fb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="162fb-111">PARAMETERS</span></span>

### <span data-ttu-id="162fb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="162fb-112">-AccountName</span></span>
<span data-ttu-id="162fb-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="162fb-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="162fb-114">-ContainerName</span></span>
<span data-ttu-id="162fb-115">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-115">Container name.</span></span>

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

### <span data-ttu-id="162fb-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="162fb-116">-DatabaseName</span></span>
<span data-ttu-id="162fb-117">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-117">Database name.</span></span>

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

### <span data-ttu-id="162fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162fb-118">-DefaultProfile</span></span>
<span data-ttu-id="162fb-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="162fb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="162fb-120">-Name</span></span>
<span data-ttu-id="162fb-121">저장된 Prcodecure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="162fb-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="162fb-122">-ParentObject</span></span>
<span data-ttu-id="162fb-123">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-123">Sql Container object.</span></span>

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

### <span data-ttu-id="162fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="162fb-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="162fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162fb-126">CommonParameters</span></span>
<span data-ttu-id="162fb-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="162fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162fb-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="162fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162fb-129">입력</span><span class="sxs-lookup"><span data-stu-id="162fb-129">INPUTS</span></span>

### <span data-ttu-id="162fb-130">없음</span><span class="sxs-lookup"><span data-stu-id="162fb-130">None</span></span>

## <span data-ttu-id="162fb-131">출력</span><span class="sxs-lookup"><span data-stu-id="162fb-131">OUTPUTS</span></span>

### <span data-ttu-id="162fb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="162fb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="162fb-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="162fb-133">NOTES</span></span>

## <span data-ttu-id="162fb-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="162fb-134">RELATED LINKS</span></span>
