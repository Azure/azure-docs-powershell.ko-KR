---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306722"
---
# <span data-ttu-id="c6922-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="c6922-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="c6922-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6922-102">SYNOPSIS</span></span>
<span data-ttu-id="c6922-103">CosmosDB 테이블의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="c6922-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6922-104">SYNTAX</span></span>

### <span data-ttu-id="c6922-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6922-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6922-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6922-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6922-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6922-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6922-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c6922-108">DESCRIPTION</span></span>
<span data-ttu-id="c6922-109">CosmosDB 테이블의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="c6922-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c6922-110">EXAMPLES</span></span>

### <span data-ttu-id="c6922-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6922-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="c6922-112">변수</span><span class="sxs-lookup"><span data-stu-id="c6922-112">PARAMETERS</span></span>

### <span data-ttu-id="c6922-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6922-113">-AccountName</span></span>
<span data-ttu-id="c6922-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c6922-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c6922-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c6922-116">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c6922-117">-확인</span><span class="sxs-lookup"><span data-stu-id="c6922-117">-Confirm</span></span>
<span data-ttu-id="c6922-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6922-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6922-119">-DefaultProfile</span></span>
<span data-ttu-id="c6922-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6922-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6922-121">-InputObject</span></span>
<span data-ttu-id="c6922-122">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="c6922-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c6922-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c6922-123">-Name</span></span>
<span data-ttu-id="c6922-124">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-124">Name of the Table.</span></span>

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

### <span data-ttu-id="c6922-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6922-125">-ParentObject</span></span>
<span data-ttu-id="c6922-126">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="c6922-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c6922-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6922-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6922-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c6922-129">-처리량</span><span class="sxs-lookup"><span data-stu-id="c6922-129">-Throughput</span></span>
<span data-ttu-id="c6922-130">테이블의 처리량 (1/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="c6922-131">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-131">Default value is 400.</span></span>

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

### <span data-ttu-id="c6922-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6922-132">-WhatIf</span></span>
<span data-ttu-id="c6922-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6922-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6922-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6922-135">CommonParameters</span></span>
<span data-ttu-id="c6922-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6922-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6922-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c6922-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6922-138">입력</span><span class="sxs-lookup"><span data-stu-id="c6922-138">INPUTS</span></span>

### <span data-ttu-id="c6922-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c6922-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c6922-140">출력</span><span class="sxs-lookup"><span data-stu-id="c6922-140">OUTPUTS</span></span>

### <span data-ttu-id="c6922-141">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c6922-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c6922-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c6922-142">NOTES</span></span>

## <span data-ttu-id="c6922-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6922-143">RELATED LINKS</span></span>
