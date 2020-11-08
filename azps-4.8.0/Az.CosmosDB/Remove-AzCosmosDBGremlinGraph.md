---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212858"
---
# <span data-ttu-id="ecda9-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="ecda9-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="ecda9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecda9-102">SYNOPSIS</span></span>
<span data-ttu-id="ecda9-103">CosmosDB Gremlin 그래프를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ecda9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecda9-104">SYNTAX</span></span>

### <span data-ttu-id="ecda9-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ecda9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecda9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecda9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecda9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ecda9-107">DESCRIPTION</span></span>
<span data-ttu-id="ecda9-108">**AzCosmosDBGremlinGraph** Cmdlet은 CosmosDB Gremlin Graph를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ecda9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ecda9-109">EXAMPLES</span></span>

### <span data-ttu-id="ecda9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecda9-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="ecda9-111">Cmdlet은 삭제가 성공한 경우 true 인 bool (-PassThru가 전달 되는 경우) 형식의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="ecda9-112">변수</span><span class="sxs-lookup"><span data-stu-id="ecda9-112">PARAMETERS</span></span>

### <span data-ttu-id="ecda9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ecda9-113">-AccountName</span></span>
<span data-ttu-id="ecda9-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ecda9-115">-확인</span><span class="sxs-lookup"><span data-stu-id="ecda9-115">-Confirm</span></span>
<span data-ttu-id="ecda9-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecda9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ecda9-117">-DatabaseName</span></span>
<span data-ttu-id="ecda9-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-118">Database name.</span></span>

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

### <span data-ttu-id="ecda9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecda9-119">-DefaultProfile</span></span>
<span data-ttu-id="ecda9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecda9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecda9-121">-InputObject</span></span>
<span data-ttu-id="ecda9-122">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecda9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ecda9-123">-Name</span></span>
<span data-ttu-id="ecda9-124">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="ecda9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecda9-125">-PassThru</span></span>
<span data-ttu-id="ecda9-126">사용자가 출력을 받으려는 경우 true로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ecda9-127">작업에 성공한 경우 출력이 true이 고, 그렇지 않은 경우 오류가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecda9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecda9-128">-ResourceGroupName</span></span>
<span data-ttu-id="ecda9-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-129">Name of resource group.</span></span>

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

### <span data-ttu-id="ecda9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecda9-130">-WhatIf</span></span>
<span data-ttu-id="ecda9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecda9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecda9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecda9-133">CommonParameters</span></span>
<span data-ttu-id="ecda9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecda9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecda9-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ecda9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecda9-136">입력</span><span class="sxs-lookup"><span data-stu-id="ecda9-136">INPUTS</span></span>

### <span data-ttu-id="ecda9-137">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="ecda9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="ecda9-138">출력</span><span class="sxs-lookup"><span data-stu-id="ecda9-138">OUTPUTS</span></span>

### <span data-ttu-id="ecda9-139">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ecda9-139">System.Void</span></span>

### <span data-ttu-id="ecda9-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ecda9-140">System.Boolean</span></span>

## <span data-ttu-id="ecda9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ecda9-141">NOTES</span></span>

## <span data-ttu-id="ecda9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecda9-142">RELATED LINKS</span></span>
