---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 56c99a1e3cf21f38544e97ee84ba10efb51bc983
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042175"
---
# <span data-ttu-id="93f05-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="93f05-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="93f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f05-102">SYNOPSIS</span></span>
<span data-ttu-id="93f05-103">CosmosDB 테이블의 처리량 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="93f05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93f05-104">SYNTAX</span></span>

### <span data-ttu-id="93f05-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="93f05-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f05-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93f05-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f05-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93f05-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -InputObject <PSTableGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93f05-108">예제의</span><span class="sxs-lookup"><span data-stu-id="93f05-108">EXAMPLES</span></span>

### <span data-ttu-id="93f05-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="93f05-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="93f05-110">변수</span><span class="sxs-lookup"><span data-stu-id="93f05-110">PARAMETERS</span></span>

### <span data-ttu-id="93f05-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93f05-111">-AccountName</span></span>
<span data-ttu-id="93f05-112">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="93f05-113">-확인</span><span class="sxs-lookup"><span data-stu-id="93f05-113">-Confirm</span></span>
<span data-ttu-id="93f05-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93f05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f05-115">-DefaultProfile</span></span>
<span data-ttu-id="93f05-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f05-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93f05-117">-InputObject</span></span>
<span data-ttu-id="93f05-118">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="93f05-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="93f05-119">-이름</span><span class="sxs-lookup"><span data-stu-id="93f05-119">-Name</span></span>
<span data-ttu-id="93f05-120">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-120">Name of the Table.</span></span>

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

### <span data-ttu-id="93f05-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="93f05-121">-ParentObject</span></span>
<span data-ttu-id="93f05-122">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="93f05-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="93f05-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f05-123">-ResourceGroupName</span></span>
<span data-ttu-id="93f05-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-124">Name of resource group.</span></span>

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

### <span data-ttu-id="93f05-125">-처리량</span><span class="sxs-lookup"><span data-stu-id="93f05-125">-Throughput</span></span>
<span data-ttu-id="93f05-126">테이블의 처리량 (1/s)입니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="93f05-127">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f05-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f05-128">-WhatIf</span></span>
<span data-ttu-id="93f05-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f05-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93f05-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f05-131">CommonParameters</span></span>
<span data-ttu-id="93f05-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93f05-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f05-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93f05-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f05-134">입력</span><span class="sxs-lookup"><span data-stu-id="93f05-134">INPUTS</span></span>

### <span data-ttu-id="93f05-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="93f05-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="93f05-136">출력</span><span class="sxs-lookup"><span data-stu-id="93f05-136">OUTPUTS</span></span>

### <span data-ttu-id="93f05-137">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="93f05-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="93f05-138">상속자</span><span class="sxs-lookup"><span data-stu-id="93f05-138">NOTES</span></span>

## <span data-ttu-id="93f05-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93f05-139">RELATED LINKS</span></span>
