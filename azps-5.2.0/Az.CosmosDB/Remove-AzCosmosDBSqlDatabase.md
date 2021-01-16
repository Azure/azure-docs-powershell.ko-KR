---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351537"
---
# <span data-ttu-id="a54f5-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a54f5-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="a54f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a54f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a54f5-103">CosmosDB Sql Database를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a54f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="a54f5-104">SYNTAX</span></span>

### <span data-ttu-id="a54f5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a54f5-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a54f5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a54f5-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a54f5-107">설명</span><span class="sxs-lookup"><span data-stu-id="a54f5-107">DESCRIPTION</span></span>
<span data-ttu-id="a54f5-108">**Remove-AzCosmosDBSqlDatabase** cmdlet은 주어진 ResourceGroupName, AccountName 및 DatabaseName에 해당하는 CosmosDB Sql Database를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="a54f5-109">예제</span><span class="sxs-lookup"><span data-stu-id="a54f5-109">EXAMPLES</span></span>

### <span data-ttu-id="a54f5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a54f5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="a54f5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a54f5-111">PARAMETERS</span></span>

### <span data-ttu-id="a54f5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a54f5-112">-AccountName</span></span>
<span data-ttu-id="a54f5-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a54f5-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a54f5-114">-Confirm</span></span>
<span data-ttu-id="a54f5-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a54f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54f5-116">-DefaultProfile</span></span>
<span data-ttu-id="a54f5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54f5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a54f5-118">-InputObject</span></span>
<span data-ttu-id="a54f5-119">Sql Database 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a54f5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a54f5-120">-Name</span></span>
<span data-ttu-id="a54f5-121">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-121">Database name.</span></span>

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

### <span data-ttu-id="a54f5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a54f5-122">-PassThru</span></span>
<span data-ttu-id="a54f5-123">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a54f5-124">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a54f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a54f5-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a54f5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a54f5-127">-WhatIf</span></span>
<span data-ttu-id="a54f5-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a54f5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a54f5-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a54f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54f5-130">CommonParameters</span></span>
<span data-ttu-id="a54f5-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a54f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54f5-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a54f5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54f5-133">입력</span><span class="sxs-lookup"><span data-stu-id="a54f5-133">INPUTS</span></span>

### <span data-ttu-id="a54f5-134">없음</span><span class="sxs-lookup"><span data-stu-id="a54f5-134">None</span></span>

## <span data-ttu-id="a54f5-135">출력</span><span class="sxs-lookup"><span data-stu-id="a54f5-135">OUTPUTS</span></span>

### <span data-ttu-id="a54f5-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="a54f5-136">System.Void</span></span>

### <span data-ttu-id="a54f5-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a54f5-137">System.Boolean</span></span>

## <span data-ttu-id="a54f5-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a54f5-138">NOTES</span></span>

## <span data-ttu-id="a54f5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a54f5-139">RELATED LINKS</span></span>