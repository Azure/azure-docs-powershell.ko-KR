---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 2a09582c57cdb06dea955dcbd1c4728b822d229c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971323"
---
# <span data-ttu-id="ed93c-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="ed93c-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="ed93c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed93c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed93c-103">CosmosDB Gremlin Database를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ed93c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed93c-104">SYNTAX</span></span>

### <span data-ttu-id="ed93c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed93c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed93c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed93c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed93c-107">설명</span><span class="sxs-lookup"><span data-stu-id="ed93c-107">DESCRIPTION</span></span>
<span data-ttu-id="ed93c-108">**Remove-AzCosmosDBGremlinDatabase** cmdlet은 CosmosDB Gremlin Database를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ed93c-109">예제</span><span class="sxs-lookup"><span data-stu-id="ed93c-109">EXAMPLES</span></span>

### <span data-ttu-id="ed93c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed93c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="ed93c-111">cmdlet은 삭제가 성공한 경우 true인 형식 bool(-PassThru가 전달될 때)의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="ed93c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed93c-112">PARAMETERS</span></span>

### <span data-ttu-id="ed93c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed93c-113">-AccountName</span></span>
<span data-ttu-id="ed93c-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ed93c-115">-확인</span><span class="sxs-lookup"><span data-stu-id="ed93c-115">-Confirm</span></span>
<span data-ttu-id="ed93c-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed93c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed93c-117">-DefaultProfile</span></span>
<span data-ttu-id="ed93c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed93c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed93c-119">-InputObject</span></span>
<span data-ttu-id="ed93c-120">Gremlin Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed93c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ed93c-121">-Name</span></span>
<span data-ttu-id="ed93c-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-122">Database name.</span></span>

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

### <span data-ttu-id="ed93c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed93c-123">-PassThru</span></span>
<span data-ttu-id="ed93c-124">사용자가 출력을 수신하려는 경우 true로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ed93c-125">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ed93c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed93c-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed93c-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-127">Name of resource group.</span></span>

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

### <span data-ttu-id="ed93c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed93c-128">-WhatIf</span></span>
<span data-ttu-id="ed93c-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed93c-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed93c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed93c-131">CommonParameters</span></span>
<span data-ttu-id="ed93c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed93c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed93c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed93c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed93c-134">입력</span><span class="sxs-lookup"><span data-stu-id="ed93c-134">INPUTS</span></span>

### <span data-ttu-id="ed93c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ed93c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="ed93c-136">출력</span><span class="sxs-lookup"><span data-stu-id="ed93c-136">OUTPUTS</span></span>

### <span data-ttu-id="ed93c-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="ed93c-137">System.Void</span></span>

### <span data-ttu-id="ed93c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed93c-138">System.Boolean</span></span>

## <span data-ttu-id="ed93c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed93c-139">NOTES</span></span>

## <span data-ttu-id="ed93c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed93c-140">RELATED LINKS</span></span>
