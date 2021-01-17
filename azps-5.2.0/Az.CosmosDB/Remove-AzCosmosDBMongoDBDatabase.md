---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350469"
---
# <span data-ttu-id="c43c6-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="c43c6-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="c43c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c43c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c43c6-103">CosmosDB MongoDB 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="c43c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="c43c6-104">SYNTAX</span></span>

### <span data-ttu-id="c43c6-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c43c6-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c43c6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c43c6-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43c6-107">설명</span><span class="sxs-lookup"><span data-stu-id="c43c6-107">DESCRIPTION</span></span>
<span data-ttu-id="c43c6-108">**Remove-AzCosmosDBMongoDBDatabase** cmdlet은 CosmosDB MongoDB 데이터베이스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="c43c6-109">예제</span><span class="sxs-lookup"><span data-stu-id="c43c6-109">EXAMPLES</span></span>

### <span data-ttu-id="c43c6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c43c6-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="c43c6-111">cmdlet은 삭제에 성공한 경우 true인 bool 형식의 개체를 반환합니다(-PassThru가 전달된 경우).</span><span class="sxs-lookup"><span data-stu-id="c43c6-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="c43c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c43c6-112">PARAMETERS</span></span>

### <span data-ttu-id="c43c6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c43c6-113">-AccountName</span></span>
<span data-ttu-id="c43c6-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c43c6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c43c6-115">-Confirm</span></span>
<span data-ttu-id="c43c6-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43c6-117">-DefaultProfile</span></span>
<span data-ttu-id="c43c6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c43c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c43c6-119">-InputObject</span></span>
<span data-ttu-id="c43c6-120">Mongo Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c43c6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c43c6-121">-Name</span></span>
<span data-ttu-id="c43c6-122">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-122">Database name.</span></span>

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

### <span data-ttu-id="c43c6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c43c6-123">-PassThru</span></span>
<span data-ttu-id="c43c6-124">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c43c6-125">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c43c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c43c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="c43c6-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-127">Name of resource group.</span></span>

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

### <span data-ttu-id="c43c6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43c6-128">-WhatIf</span></span>
<span data-ttu-id="c43c6-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c43c6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c43c6-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43c6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43c6-131">CommonParameters</span></span>
<span data-ttu-id="c43c6-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c43c6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43c6-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c43c6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43c6-134">입력</span><span class="sxs-lookup"><span data-stu-id="c43c6-134">INPUTS</span></span>

### <span data-ttu-id="c43c6-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c43c6-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="c43c6-136">출력</span><span class="sxs-lookup"><span data-stu-id="c43c6-136">OUTPUTS</span></span>

### <span data-ttu-id="c43c6-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="c43c6-137">System.Void</span></span>

### <span data-ttu-id="c43c6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c43c6-138">System.Boolean</span></span>

## <span data-ttu-id="c43c6-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c43c6-139">NOTES</span></span>

## <span data-ttu-id="c43c6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c43c6-140">RELATED LINKS</span></span>
