---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352785"
---
# <span data-ttu-id="61eeb-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="61eeb-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="61eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="61eeb-103">CosmosDB Sql UserDefinedFunction을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="61eeb-104">구문</span><span class="sxs-lookup"><span data-stu-id="61eeb-104">SYNTAX</span></span>

### <span data-ttu-id="61eeb-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eeb-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eeb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eeb-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61eeb-107">설명</span><span class="sxs-lookup"><span data-stu-id="61eeb-107">DESCRIPTION</span></span>
<span data-ttu-id="61eeb-108">**Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet은 주어진 ResourceGroupName, AccountName 및 DatabaseName에 해당하는 CosmosDB Sql UserDefinedFunction을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="61eeb-109">예제</span><span class="sxs-lookup"><span data-stu-id="61eeb-109">EXAMPLES</span></span>

### <span data-ttu-id="61eeb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="61eeb-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="61eeb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61eeb-111">PARAMETERS</span></span>

### <span data-ttu-id="61eeb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61eeb-112">-AccountName</span></span>
<span data-ttu-id="61eeb-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61eeb-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61eeb-114">-Confirm</span></span>
<span data-ttu-id="61eeb-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61eeb-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="61eeb-116">-ContainerName</span></span>
<span data-ttu-id="61eeb-117">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-117">Container name.</span></span>

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

### <span data-ttu-id="61eeb-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61eeb-118">-DatabaseName</span></span>
<span data-ttu-id="61eeb-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-119">Database name.</span></span>

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

### <span data-ttu-id="61eeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61eeb-120">-DefaultProfile</span></span>
<span data-ttu-id="61eeb-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61eeb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61eeb-122">-InputObject</span></span>
<span data-ttu-id="61eeb-123">Sql 사용자 정의 함수 개체</span><span class="sxs-lookup"><span data-stu-id="61eeb-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61eeb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="61eeb-124">-Name</span></span>
<span data-ttu-id="61eeb-125">사용자 정의 함수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="61eeb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61eeb-126">-PassThru</span></span>
<span data-ttu-id="61eeb-127">사용자가 출력을 수신하려는 경우 true로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="61eeb-128">작업이 성공하고 그렇지 않은 경우 오류가 throw된 경우 출력이 true입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="61eeb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61eeb-129">-ResourceGroupName</span></span>
<span data-ttu-id="61eeb-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-130">Name of resource group.</span></span>

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

### <span data-ttu-id="61eeb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61eeb-131">-WhatIf</span></span>
<span data-ttu-id="61eeb-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="61eeb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61eeb-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61eeb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61eeb-134">CommonParameters</span></span>
<span data-ttu-id="61eeb-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61eeb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61eeb-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61eeb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61eeb-137">입력</span><span class="sxs-lookup"><span data-stu-id="61eeb-137">INPUTS</span></span>

### <span data-ttu-id="61eeb-138">없음</span><span class="sxs-lookup"><span data-stu-id="61eeb-138">None</span></span>

## <span data-ttu-id="61eeb-139">출력</span><span class="sxs-lookup"><span data-stu-id="61eeb-139">OUTPUTS</span></span>

### <span data-ttu-id="61eeb-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="61eeb-140">System.Void</span></span>

### <span data-ttu-id="61eeb-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61eeb-141">System.Boolean</span></span>

## <span data-ttu-id="61eeb-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61eeb-142">NOTES</span></span>

## <span data-ttu-id="61eeb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61eeb-143">RELATED LINKS</span></span>
