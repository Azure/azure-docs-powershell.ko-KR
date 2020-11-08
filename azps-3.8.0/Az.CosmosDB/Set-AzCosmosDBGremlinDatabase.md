---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044436"
---
# <span data-ttu-id="2b723-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="2b723-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="2b723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b723-102">SYNOPSIS</span></span>
<span data-ttu-id="2b723-103">CosmosDB Gremlin 데이터베이스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="2b723-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b723-104">SYNTAX</span></span>

### <span data-ttu-id="2b723-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b723-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b723-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b723-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b723-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2b723-107">DESCRIPTION</span></span>
<span data-ttu-id="2b723-108">**Set-AzCosmosDBGremlinDatabase** Cmdlet은 CosmosDB Gremlin 데이터베이스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="2b723-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2b723-109">EXAMPLES</span></span>

### <span data-ttu-id="2b723-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b723-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="2b723-111">리소스 개체에 _rid, _ts _etag 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="2b723-112">변수</span><span class="sxs-lookup"><span data-stu-id="2b723-112">PARAMETERS</span></span>

### <span data-ttu-id="2b723-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b723-113">-AccountName</span></span>
<span data-ttu-id="2b723-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2b723-115">-확인</span><span class="sxs-lookup"><span data-stu-id="2b723-115">-Confirm</span></span>
<span data-ttu-id="2b723-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b723-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b723-117">-DefaultProfile</span></span>
<span data-ttu-id="2b723-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b723-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b723-119">-InputObject</span></span>
<span data-ttu-id="2b723-120">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="2b723-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2b723-121">-이름</span><span class="sxs-lookup"><span data-stu-id="2b723-121">-Name</span></span>
<span data-ttu-id="2b723-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-122">Database name.</span></span>

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

### <span data-ttu-id="2b723-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b723-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b723-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-124">Name of resource group.</span></span>

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

### <span data-ttu-id="2b723-125">-처리량</span><span class="sxs-lookup"><span data-stu-id="2b723-125">-Throughput</span></span>
<span data-ttu-id="2b723-126">Gremlin 데이터베이스의 처리량 (. e 1/s)</span><span class="sxs-lookup"><span data-stu-id="2b723-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="2b723-127">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-127">Default value is 400.</span></span>

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

### <span data-ttu-id="2b723-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b723-128">-WhatIf</span></span>
<span data-ttu-id="2b723-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b723-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b723-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b723-131">CommonParameters</span></span>
<span data-ttu-id="2b723-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b723-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b723-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b723-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b723-134">입력</span><span class="sxs-lookup"><span data-stu-id="2b723-134">INPUTS</span></span>

### <span data-ttu-id="2b723-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2b723-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2b723-136">출력</span><span class="sxs-lookup"><span data-stu-id="2b723-136">OUTPUTS</span></span>

### <span data-ttu-id="2b723-137">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="2b723-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="2b723-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2b723-138">NOTES</span></span>

## <span data-ttu-id="2b723-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b723-139">RELATED LINKS</span></span>
