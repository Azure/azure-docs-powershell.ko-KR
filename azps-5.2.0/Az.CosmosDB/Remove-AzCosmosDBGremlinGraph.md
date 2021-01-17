---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350486"
---
# <span data-ttu-id="70885-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="70885-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="70885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70885-102">SYNOPSIS</span></span>
<span data-ttu-id="70885-103">CosmosDB Gremlin Graph를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="70885-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="70885-104">구문</span><span class="sxs-lookup"><span data-stu-id="70885-104">SYNTAX</span></span>

### <span data-ttu-id="70885-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="70885-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70885-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70885-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70885-107">설명</span><span class="sxs-lookup"><span data-stu-id="70885-107">DESCRIPTION</span></span>
<span data-ttu-id="70885-108">**Remove-AzCosmosDBGremlinGraph** cmdlet은 CosmosDB Gremlin Graph를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="70885-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="70885-109">예제</span><span class="sxs-lookup"><span data-stu-id="70885-109">EXAMPLES</span></span>

### <span data-ttu-id="70885-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="70885-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="70885-111">cmdlet은 삭제에 성공한 경우 true인 bool 형식의 개체를 반환합니다(-PassThru가 전달된 경우).</span><span class="sxs-lookup"><span data-stu-id="70885-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="70885-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70885-112">PARAMETERS</span></span>

### <span data-ttu-id="70885-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70885-113">-AccountName</span></span>
<span data-ttu-id="70885-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="70885-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70885-115">-Confirm</span></span>
<span data-ttu-id="70885-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="70885-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70885-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70885-117">-DatabaseName</span></span>
<span data-ttu-id="70885-118">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-118">Database name.</span></span>

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

### <span data-ttu-id="70885-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70885-119">-DefaultProfile</span></span>
<span data-ttu-id="70885-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70885-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70885-121">-InputObject</span></span>
<span data-ttu-id="70885-122">Gremlin Graph 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="70885-123">-Name</span><span class="sxs-lookup"><span data-stu-id="70885-123">-Name</span></span>
<span data-ttu-id="70885-124">Gremlin Graph 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="70885-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70885-125">-PassThru</span></span>
<span data-ttu-id="70885-126">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="70885-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="70885-127">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="70885-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70885-128">-ResourceGroupName</span></span>
<span data-ttu-id="70885-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70885-129">Name of resource group.</span></span>

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

### <span data-ttu-id="70885-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70885-130">-WhatIf</span></span>
<span data-ttu-id="70885-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="70885-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70885-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70885-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70885-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70885-133">CommonParameters</span></span>
<span data-ttu-id="70885-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="70885-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70885-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70885-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70885-136">입력</span><span class="sxs-lookup"><span data-stu-id="70885-136">INPUTS</span></span>

### <span data-ttu-id="70885-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="70885-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="70885-138">출력</span><span class="sxs-lookup"><span data-stu-id="70885-138">OUTPUTS</span></span>

### <span data-ttu-id="70885-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="70885-139">System.Void</span></span>

### <span data-ttu-id="70885-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70885-140">System.Boolean</span></span>

## <span data-ttu-id="70885-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="70885-141">NOTES</span></span>

## <span data-ttu-id="70885-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70885-142">RELATED LINKS</span></span>
