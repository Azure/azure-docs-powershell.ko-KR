---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212563"
---
# <span data-ttu-id="97531-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="97531-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="97531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97531-102">SYNOPSIS</span></span>
<span data-ttu-id="97531-103">새 CosmosDB 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97531-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="97531-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97531-104">SYNTAX</span></span>

### <span data-ttu-id="97531-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="97531-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97531-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97531-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97531-107">설명은</span><span class="sxs-lookup"><span data-stu-id="97531-107">DESCRIPTION</span></span>
<span data-ttu-id="97531-108">새 CosmosDB 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="97531-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="97531-109">예제의</span><span class="sxs-lookup"><span data-stu-id="97531-109">EXAMPLES</span></span>

### <span data-ttu-id="97531-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="97531-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="97531-111">변수</span><span class="sxs-lookup"><span data-stu-id="97531-111">PARAMETERS</span></span>

### <span data-ttu-id="97531-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97531-112">-AccountName</span></span>
<span data-ttu-id="97531-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="97531-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="97531-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="97531-115">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="97531-116">-확인</span><span class="sxs-lookup"><span data-stu-id="97531-116">-Confirm</span></span>
<span data-ttu-id="97531-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="97531-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97531-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97531-118">-DefaultProfile</span></span>
<span data-ttu-id="97531-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97531-120">-이름</span><span class="sxs-lookup"><span data-stu-id="97531-120">-Name</span></span>
<span data-ttu-id="97531-121">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-121">Name of the Table.</span></span>

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

### <span data-ttu-id="97531-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="97531-122">-ParentObject</span></span>
<span data-ttu-id="97531-123">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="97531-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="97531-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97531-124">-ResourceGroupName</span></span>
<span data-ttu-id="97531-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-125">Name of resource group.</span></span>

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

### <span data-ttu-id="97531-126">-처리량</span><span class="sxs-lookup"><span data-stu-id="97531-126">-Throughput</span></span>
<span data-ttu-id="97531-127">테이블의 처리량 (1/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="97531-128">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="97531-128">Default value is 400.</span></span>

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

### <span data-ttu-id="97531-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97531-129">-WhatIf</span></span>
<span data-ttu-id="97531-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="97531-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97531-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97531-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97531-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97531-132">CommonParameters</span></span>
<span data-ttu-id="97531-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97531-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97531-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97531-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97531-135">입력</span><span class="sxs-lookup"><span data-stu-id="97531-135">INPUTS</span></span>

### <span data-ttu-id="97531-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="97531-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="97531-137">출력</span><span class="sxs-lookup"><span data-stu-id="97531-137">OUTPUTS</span></span>

### <span data-ttu-id="97531-138">CosmosDB. PSTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="97531-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="97531-139">CosmosDB (ConflictingResourceException).</span><span class="sxs-lookup"><span data-stu-id="97531-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="97531-140">상속자</span><span class="sxs-lookup"><span data-stu-id="97531-140">NOTES</span></span>

## <span data-ttu-id="97531-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97531-141">RELATED LINKS</span></span>
