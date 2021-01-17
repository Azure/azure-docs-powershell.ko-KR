---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372891"
---
# <span data-ttu-id="cd822-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="cd822-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="cd822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd822-102">SYNOPSIS</span></span>
<span data-ttu-id="cd822-103">CosmosDB 테이블의 진행 값도 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="cd822-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd822-104">SYNTAX</span></span>

### <span data-ttu-id="cd822-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd822-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd822-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd822-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd822-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd822-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd822-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd822-108">DESCRIPTION</span></span>
<span data-ttu-id="cd822-109">CosmosDB 테이블의 진행 값도 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="cd822-110">예제</span><span class="sxs-lookup"><span data-stu-id="cd822-110">EXAMPLES</span></span>

### <span data-ttu-id="cd822-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd822-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="cd822-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd822-112">PARAMETERS</span></span>

### <span data-ttu-id="cd822-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cd822-113">-AccountName</span></span>
<span data-ttu-id="cd822-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cd822-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="cd822-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="cd822-116">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="cd822-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd822-117">-Confirm</span></span>
<span data-ttu-id="cd822-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd822-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd822-119">-DefaultProfile</span></span>
<span data-ttu-id="cd822-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd822-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd822-121">-InputObject</span></span>
<span data-ttu-id="cd822-122">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="cd822-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="cd822-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cd822-123">-Name</span></span>
<span data-ttu-id="cd822-124">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-124">Name of the Table.</span></span>

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

### <span data-ttu-id="cd822-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cd822-125">-ParentObject</span></span>
<span data-ttu-id="cd822-126">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="cd822-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="cd822-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd822-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd822-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-128">Name of resource group.</span></span>

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

### <span data-ttu-id="cd822-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="cd822-129">-Throughput</span></span>
<span data-ttu-id="cd822-130">테이블의 경우(RU/s)</span><span class="sxs-lookup"><span data-stu-id="cd822-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="cd822-131">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-131">Default value is 400.</span></span>

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

### <span data-ttu-id="cd822-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd822-132">-WhatIf</span></span>
<span data-ttu-id="cd822-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cd822-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd822-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd822-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd822-135">CommonParameters</span></span>
<span data-ttu-id="cd822-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd822-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd822-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd822-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd822-138">입력</span><span class="sxs-lookup"><span data-stu-id="cd822-138">INPUTS</span></span>

### <span data-ttu-id="cd822-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="cd822-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="cd822-140">출력</span><span class="sxs-lookup"><span data-stu-id="cd822-140">OUTPUTS</span></span>

### <span data-ttu-id="cd822-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cd822-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cd822-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd822-142">NOTES</span></span>

## <span data-ttu-id="cd822-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd822-143">RELATED LINKS</span></span>
