---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: d2a4dacb929587fb0f06c002ad26df3144f32f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960795"
---
# <span data-ttu-id="25d76-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="25d76-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="25d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d76-102">SYNOPSIS</span></span>
<span data-ttu-id="25d76-103">새 CosmosDB 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="25d76-104">구문</span><span class="sxs-lookup"><span data-stu-id="25d76-104">SYNTAX</span></span>

### <span data-ttu-id="25d76-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="25d76-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25d76-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25d76-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25d76-107">설명</span><span class="sxs-lookup"><span data-stu-id="25d76-107">DESCRIPTION</span></span>
<span data-ttu-id="25d76-108">새 CosmosDB 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="25d76-109">예제</span><span class="sxs-lookup"><span data-stu-id="25d76-109">EXAMPLES</span></span>

### <span data-ttu-id="25d76-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="25d76-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="25d76-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="25d76-111">PARAMETERS</span></span>

### <span data-ttu-id="25d76-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="25d76-112">-AccountName</span></span>
<span data-ttu-id="25d76-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="25d76-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="25d76-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="25d76-115">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="25d76-116">-확인</span><span class="sxs-lookup"><span data-stu-id="25d76-116">-Confirm</span></span>
<span data-ttu-id="25d76-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d76-118">-DefaultProfile</span></span>
<span data-ttu-id="25d76-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d76-120">-Name</span><span class="sxs-lookup"><span data-stu-id="25d76-120">-Name</span></span>
<span data-ttu-id="25d76-121">표의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-121">Name of the Table.</span></span>

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

### <span data-ttu-id="25d76-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="25d76-122">-ParentObject</span></span>
<span data-ttu-id="25d76-123">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="25d76-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="25d76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d76-124">-ResourceGroupName</span></span>
<span data-ttu-id="25d76-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-125">Name of resource group.</span></span>

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

### <span data-ttu-id="25d76-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="25d76-126">-Throughput</span></span>
<span data-ttu-id="25d76-127">테이블(RU/s)의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="25d76-128">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-128">Default value is 400.</span></span>

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

### <span data-ttu-id="25d76-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d76-129">-WhatIf</span></span>
<span data-ttu-id="25d76-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d76-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d76-132">CommonParameters</span></span>
<span data-ttu-id="25d76-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25d76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d76-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25d76-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d76-135">입력</span><span class="sxs-lookup"><span data-stu-id="25d76-135">INPUTS</span></span>

### <span data-ttu-id="25d76-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="25d76-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="25d76-137">출력</span><span class="sxs-lookup"><span data-stu-id="25d76-137">OUTPUTS</span></span>

### <span data-ttu-id="25d76-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="25d76-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="25d76-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="25d76-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="25d76-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25d76-140">NOTES</span></span>

## <span data-ttu-id="25d76-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25d76-141">RELATED LINKS</span></span>
