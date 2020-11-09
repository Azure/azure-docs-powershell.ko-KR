---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307160"
---
# <span data-ttu-id="9a1f5-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="9a1f5-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="9a1f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1f5-103">이를 사용 하 여 자동 크기 조정 처리량을 수동 처리량으로 마이그레이션하고 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="9a1f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a1f5-104">SYNTAX</span></span>

### <span data-ttu-id="9a1f5-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a1f5-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1f5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1f5-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a1f5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a1f5-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a1f5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a1f5-108">DESCRIPTION</span></span>
<span data-ttu-id="9a1f5-109">ThroughpyteType 매개 변수는 마이그레이션할 처리량을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="9a1f5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9a1f5-110">EXAMPLES</span></span>

### <span data-ttu-id="9a1f5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a1f5-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="9a1f5-112">변수</span><span class="sxs-lookup"><span data-stu-id="9a1f5-112">PARAMETERS</span></span>

### <span data-ttu-id="9a1f5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9a1f5-113">-AccountName</span></span>
<span data-ttu-id="9a1f5-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9a1f5-115">-확인</span><span class="sxs-lookup"><span data-stu-id="9a1f5-115">-Confirm</span></span>
<span data-ttu-id="9a1f5-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a1f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a1f5-117">-DefaultProfile</span></span>
<span data-ttu-id="9a1f5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a1f5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a1f5-119">-InputObject</span></span>
<span data-ttu-id="9a1f5-120">테이블 개체</span><span class="sxs-lookup"><span data-stu-id="9a1f5-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a1f5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9a1f5-121">-Name</span></span>
<span data-ttu-id="9a1f5-122">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-122">Name of the Table.</span></span>

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

### <span data-ttu-id="9a1f5-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a1f5-123">-ParentObject</span></span>
<span data-ttu-id="9a1f5-124">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="9a1f5-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9a1f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a1f5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9a1f5-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="9a1f5-127">-ThroughputType</span></span>
<span data-ttu-id="9a1f5-128">마이그레이션할 처리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="9a1f5-129">사용할 수 있는 값은 자동 크기 조정, 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="9a1f5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a1f5-130">-WhatIf</span></span>
<span data-ttu-id="9a1f5-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a1f5-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a1f5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1f5-133">CommonParameters</span></span>
<span data-ttu-id="9a1f5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1f5-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1f5-136">입력</span><span class="sxs-lookup"><span data-stu-id="9a1f5-136">INPUTS</span></span>

### <span data-ttu-id="9a1f5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="9a1f5-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="9a1f5-138">CosmosDB. PSTableGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="9a1f5-139">출력</span><span class="sxs-lookup"><span data-stu-id="9a1f5-139">OUTPUTS</span></span>

### <span data-ttu-id="9a1f5-140">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9a1f5-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9a1f5-141">NOTES</span></span>

## <span data-ttu-id="9a1f5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a1f5-142">RELATED LINKS</span></span>
