---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495771"
---
# <span data-ttu-id="37cf7-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="37cf7-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="37cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="37cf7-103">새 CosmosDB 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="37cf7-104">구문</span><span class="sxs-lookup"><span data-stu-id="37cf7-104">SYNTAX</span></span>

### <span data-ttu-id="37cf7-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="37cf7-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cf7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37cf7-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37cf7-107">설명</span><span class="sxs-lookup"><span data-stu-id="37cf7-107">DESCRIPTION</span></span>
<span data-ttu-id="37cf7-108">새 CosmosDB 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="37cf7-109">예제</span><span class="sxs-lookup"><span data-stu-id="37cf7-109">EXAMPLES</span></span>

### <span data-ttu-id="37cf7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="37cf7-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="37cf7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37cf7-111">PARAMETERS</span></span>

### <span data-ttu-id="37cf7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="37cf7-112">-AccountName</span></span>
<span data-ttu-id="37cf7-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="37cf7-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="37cf7-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="37cf7-115">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="37cf7-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37cf7-116">-Confirm</span></span>
<span data-ttu-id="37cf7-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cf7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cf7-118">-DefaultProfile</span></span>
<span data-ttu-id="37cf7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37cf7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="37cf7-120">-Name</span></span>
<span data-ttu-id="37cf7-121">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-121">Name of the Table.</span></span>

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

### <span data-ttu-id="37cf7-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37cf7-122">-ParentObject</span></span>
<span data-ttu-id="37cf7-123">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="37cf7-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="37cf7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cf7-124">-ResourceGroupName</span></span>
<span data-ttu-id="37cf7-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-125">Name of resource group.</span></span>

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

### <span data-ttu-id="37cf7-126">-Throughput</span><span class="sxs-lookup"><span data-stu-id="37cf7-126">-Throughput</span></span>
<span data-ttu-id="37cf7-127">테이블의 경우(RU/s)</span><span class="sxs-lookup"><span data-stu-id="37cf7-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="37cf7-128">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-128">Default value is 400.</span></span>

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

### <span data-ttu-id="37cf7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cf7-129">-WhatIf</span></span>
<span data-ttu-id="37cf7-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37cf7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cf7-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cf7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cf7-132">CommonParameters</span></span>
<span data-ttu-id="37cf7-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37cf7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cf7-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37cf7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cf7-135">입력</span><span class="sxs-lookup"><span data-stu-id="37cf7-135">INPUTS</span></span>

### <span data-ttu-id="37cf7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="37cf7-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="37cf7-137">출력</span><span class="sxs-lookup"><span data-stu-id="37cf7-137">OUTPUTS</span></span>

### <span data-ttu-id="37cf7-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="37cf7-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="37cf7-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="37cf7-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="37cf7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37cf7-140">NOTES</span></span>

## <span data-ttu-id="37cf7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37cf7-141">RELATED LINKS</span></span>
