---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034016"
---
# <span data-ttu-id="79132-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="79132-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="79132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79132-102">SYNOPSIS</span></span>
<span data-ttu-id="79132-103">새 CosmosDB를 만들거나 기존 Sql 데이터베이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79132-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="79132-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79132-104">SYNTAX</span></span>

### <span data-ttu-id="79132-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="79132-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79132-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79132-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79132-107">설명은</span><span class="sxs-lookup"><span data-stu-id="79132-107">DESCRIPTION</span></span>
<span data-ttu-id="79132-108">**Set-AzCosmosDBSqlDatabase** cmdlet은 새 CosmosDB Sql 데이터베이스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79132-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="79132-109">예제의</span><span class="sxs-lookup"><span data-stu-id="79132-109">EXAMPLES</span></span>

### <span data-ttu-id="79132-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="79132-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="79132-111">변수</span><span class="sxs-lookup"><span data-stu-id="79132-111">PARAMETERS</span></span>

### <span data-ttu-id="79132-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79132-112">-AccountName</span></span>
<span data-ttu-id="79132-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79132-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79132-114">-확인</span><span class="sxs-lookup"><span data-stu-id="79132-114">-Confirm</span></span>
<span data-ttu-id="79132-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79132-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79132-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79132-116">-DefaultProfile</span></span>
<span data-ttu-id="79132-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79132-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79132-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79132-118">-InputObject</span></span>
<span data-ttu-id="79132-119">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="79132-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79132-120">-이름</span><span class="sxs-lookup"><span data-stu-id="79132-120">-Name</span></span>
<span data-ttu-id="79132-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79132-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79132-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79132-122">-ResourceGroupName</span></span>
<span data-ttu-id="79132-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79132-123">Name of resource group.</span></span>

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

### <span data-ttu-id="79132-124">-처리량</span><span class="sxs-lookup"><span data-stu-id="79132-124">-Throughput</span></span>
<span data-ttu-id="79132-125">SQL 데이터베이스의 처리량 (#/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="79132-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="79132-126">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="79132-126">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79132-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79132-127">-WhatIf</span></span>
<span data-ttu-id="79132-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79132-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79132-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79132-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79132-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79132-130">CommonParameters</span></span>
<span data-ttu-id="79132-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79132-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79132-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79132-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79132-133">입력</span><span class="sxs-lookup"><span data-stu-id="79132-133">INPUTS</span></span>

### <span data-ttu-id="79132-134">않아야</span><span class="sxs-lookup"><span data-stu-id="79132-134">None</span></span>

## <span data-ttu-id="79132-135">출력</span><span class="sxs-lookup"><span data-stu-id="79132-135">OUTPUTS</span></span>

### <span data-ttu-id="79132-136">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="79132-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="79132-137">상속자</span><span class="sxs-lookup"><span data-stu-id="79132-137">NOTES</span></span>

## <span data-ttu-id="79132-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79132-138">RELATED LINKS</span></span>
